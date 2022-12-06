---
title: "Consumers"
description: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "concepts-architecture"
weight: 210
toc: true
---

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>


## Overview

A consumer is a process that attaches to a topic with a subscription and then receives messages.
A consumer first asks the Node to connect, if the node can do the authorization and validation of the requested consumer it will connect the consumer, and thats it. Node will take care to push messages to the Consumer. There are no need to configure the queue size. If a message arrives from the Producers to the Node, Node will persist the message and it will push it to the consumers that are connected. While storing the message the Andy X will update the entries and the non-connected consumers in offline subscription will know where to start consuming. Subscriptions works asynchronously from the Topic, the number of subscription do not affect the performance of Andy X.

Consumers in Andy X can do **sync** and **async** receiveing of messages, which can be achived by **two modes** that consumers works on.

Already, in Andy X there are three types of subscriptions for consumers. These types tells the Nodes how to send messages to that Consumer.

### Unique
In Unique type, only a single consumer is allowed to attach to the topic. If multiple consumers subscribe to a topic using the same consumer name, an error occurs.

### Shared
In shared or round robin type, multiple consumers can attach to the same topic. Messages are delivered in a round robin distribution across consumers, and any given message is delivered to only one consumer. When a consumer disconnects, all the messages that were sent to it and not acknowledged will be rescheduled for sending to the remaining consumers.

### Failover
Failover type, is Exclusive type with a failover consumer. If the first consumer is disconencted or faild to consume the message, node will contine pushing messages to that fail-over consumer.

## Modes

All three types of consumer connection types to a subscription described above can work in two different modes. These modes tells how a consumer will accept the messages. These modes are **Resilient** and **NonResilient**

### Resilient

In **Resilient Mode**, Andy X will send a message at a time to a consumer connected to a subscription, and waits for the confirmation from the consumer if had acknowledged the message. In case if the consumer unacknowledge a message, the node will re-send the same message until the consumer will skip or acknowledge it. If consumers are connected to a shared subscription, if one of the instances will not acknowledge, skip or unacknowledge the message, the flow of messages will break and it will require to restart consumers. This mode is designed in this way for *mission-critical* use-cases like in *Financial Systems*. ***This mode guaranties that the messages will be processed from consumers in the corrent order, with no message loss***.

### Non-resilient

In **Non-resilient Mode**, Andy X will continue to send messages as fllow of data to a connected consumer. In this case, back-pressure should be configured in the consumer side, since Andy X can transmit *milions of messages/second*. If the messsage is not acknowledged, in the server side the message will be flaged, and the messages will continue flowing towards the consumer. If you may ask, What will happen with un-acknowledged messages?
These messages will re-send again when the non-delivered yet messages are processed by the consumer and all messages are reported as acked or skipped. This mode will guarantie performance +100 times better than Resilient-Mode. *The only drawback is the the messages can be processed out-of-order, only for **Shard Subscription***.

Both modes supports at-least only ones a message will be transmitted to a consumer.


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


## Simple Consumer

Below you will find a simple code example how to create a new consumer which it requires to create a XClient object

```csharp
var consumer = Consumer<string, MessageExample>.CreateNewConsumer(xClient)
    .ForComponent("streams-examples")
    .AndTopic("sink-topic")
    .WithName("sink-topic-consumer")
    .AndSubscription(subscription =>
    {
        subscription.Name = "unique-nonresilient-subscription";
        subscription.Type = Andy.X.Client.Configurations.SubscriptionType.Unique;
        subscription.Mode = Andy.X.Client.Configurations.SubscriptionMode.NonResilient;
        subscription.InitialPosition = Andy.X.Client.Configurations.InitialPosition.Earliest;
    })
    .Build();

consumer.MessageReceivedHandler((key, message) =>
{
    Console.WriteLine($"Message received, key:{key}; messageValue:{message.Payload.Text}; entryId:{message.EntryId}; nodeId:{message.NodeId}");
    
    // acknowledge the message
    consumer.AcknowledgeMessage(message);
});

await consumer.SubscribeAsync();


```
