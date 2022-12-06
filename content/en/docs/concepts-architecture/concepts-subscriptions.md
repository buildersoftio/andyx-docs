---
title: "Subscriptions"
description: "A subscription is a named configuration rule that determines how messages are delivered to consumers."
lead: "A subscription is a named configuration rule that determines how messages are delivered to consumers."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "concepts-architecture"
weight: 209
toc: true
---

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Overview

A subscription is a named configuration rule that determines how messages are delivered to consumers. Three subscription types are available in Andy X: **unique**, **failover** and **shared**.
These types are illustrated in the figure below.
<center><img src="/images/andyx-subscriptions-types.png" style="margin-top: 40px; margin-bottom: 40px" alt="Subscription Types" align="middle"></center>

### Pub-Sub or Queuing

In Andy X, you can use different subscriptions flexibly.

* If you want to achieve traditional "fan-out pub-sub messaging" among consumers, specify a unique subscription name for each consumer. It is **unique** subscription type.
* If you want to achieve "message queuing" among consumers, share the same subscription name among multiple consumers(shared or failover).
* If you want to achieve both effects simultaneously, combine exclusive subscription type with other subscription types for consumers.

## Subscription types

When a subscription is created it has no consumers, to create a subscription is needed to define the subscription type. The subscription type can not be changed until is deleted and re-created with different subscription type.

### Unique

In Unique type, only a single consumer is allowed to attach to the subscription. If multiple consumers subscribe to a topic using the same subscription, an error occurs.
In the diagram below, only Consumer 1-0 is allowed to consume messages.
<center><img src="/images/andyx-subscriptions-unique.png" style="margin-top: 40px; margin-bottom: 40px" alt="Unique Type" align="middle"></center>

> ***Unique is the default subscription type***.

### Failover

In Failover type, multiple consumers can attach to the same subscription. A master consumer is picked for non-sharded topic or each shard of sharded topic and receives messages. When the master consumer disconnects, all (non-acknowledged and subsequent) messages are delivered to the next consumer in line.

For non-sharded topic, node will pick consumer in the order they subscribe to the non-sharded topic.

For sharded topics, node will sort consumers by priority level and lexicographical order of consumer name. Then node will try to evenly assigns topics to consumers with the highest priority level.

In the diagram below, Consumer-2-0 is the master consumer while Consumer-2-1 would be the next consumer in line to receive messages if Consumer-2-0 is disconnected.
<center><img src="/images/andyx-subscriptions-failover.png" style="margin-top: 40px; margin-bottom: 40px" alt="Failover Type" align="middle"></center>

### Shared

In shared or round robin type, multiple consumers can attach to the same subscription. Messages are delivered in a round robin distribution across consumers, and any given message is delivered to only one consumer. When a consumer disconnects, all the messages that were sent to it and not acknowledged will be rescheduled for sending to the remaining consumers.

In the diagram below, Consumer-3-1 and Consumer-3-2 are able to subscribe to the topic, but Consumer-3-3 and others could as well.

<center><img src="/images/andyx-subscriptions-shared.png" style="margin-top: 40px; margin-bottom: 40px" alt="Shared Type" align="middle"></center>

> **Limitations of Shared type**:
> When using Shared type, be aware that:
> 
> * Message ordering is not guaranteed.


## Subscription modes

All three types of consumer connection types to a subscription described above can work in two different modes. These modes tells how a consumer will accept the messages. These modes are **Resilient** and **NonResilient**

### What is a subscription mode?

The subscription mode indicates the entry-log position.
* How messages are delivered from the node.
* When a subscription is created, an associated cursor is created to record the last consumed position.
* When a consumer of the subscription restarts, it can continue consuming from the last message it consumes.

### Resilient

In **Resilient Mode**, Andy X will send a message at a time to a consumer connected to a subscription, and waits for the confirmation from the consumer if had acknowledged the message. In case if the consumer unacknowledge a message, the node will re-send the same message until the consumer will skip or acknowledge it. If consumers are connected to a shared subscription, if one of the instances will not acknowledge, skip or unacknowledge the message, the flow of messages will break and it will require to restart consumers. This mode is designed in this way for *mission-critical* use-cases like in *Financial Systems*. ***This mode guaranties that the messages will be processed from consumers in the corrent order, with no message loss***.

### Non-resilient

In **Non-resilient Mode**, Andy X will continue to send messages as fllow of data to a connected consumer. In this case, back-pressure should be configured in the consumer side, since Andy X can transmit *milions of messages/second*. If the messsage is not acknowledged, in the server side the message will be flaged, and the messages will continue flowing towards the consumer. If you may ask, What will happen with un-acknowledged messages?
These messages will re-send again when the non-delivered yet messages are processed by the consumer and all messages are reported as acked or skipped. This mode will guarantie performance +100 times better than Resilient-Mode. *The only drawback is the the messages can be processed out-of-order, only for **Shard Subscription***.

Both modes supports at-least only ones a message will be transmitted to a consumer.


A subscription can have one or more consumers. When a consumer subscribes to a topic, it must specify the subscription name. A resilient subscription and a non-resilient subscription cannot have the same name. If a consumer specifies a subscription which does not exist before, the subscription is automatically created with default values.
> ***Resilient is the default subscription mode***.

## Acknowledgement
The consumer sends an acknowledgement request to the Node after it consumes a message successfully.
Then, this consumed message will be permanently stored, and be deleted only after all the subscriptions have acknowledged it based in two  Retention Policies that Andy X supports (SOFT_TTL and HARD_TTL).

Messages can be acknowledged only individually. With individual acknowledgement, the consumer acknowledges each message and sends an acknowledgement request to the Node.
Using Andy X Client APIs there are three Acknowledgement Messages

* **Acknowledged**
* **Skipped**
* **Unacknowledged**

### Acknowledged

Using Andy X Client APIs, if the consumer will request Acknowledgement to Andy X as **Message Acknowledged**, the *subscription entry position* will change to the entry of the message already Acknowledged. Node will continue sending the next message to process to the consumer.

### Skipped

Using Andy X Client APIs, if the consumer will request Acknowledgement to Andy X as **Message Skipped**, the message will be flaged as skipped in the subscription. *Subscription entry position* will change to the next entry for the next message to be processed.

### Unacknowledged

Using Andy X Client APIs, if the consumer will request Acknowledgement to Andy X as **Message Unacknowledged**. In *Resilient Mode*, the same message will be send to process again to the Consumer. In *Nonresilient Mode*, the *MessageEntryId* will be stored into **Subscription Unacked ChangeLog** and it will stay there till the rest of messages are *Consumed* and *Acknowledged*. *If there are no new messages, Node will start producing un-acked messages from the Subscription Unacked ChangeLog*.
