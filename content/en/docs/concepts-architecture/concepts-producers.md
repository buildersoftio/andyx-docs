---
title: "Producers"
description: "A producer is a process that attaches to a topic and publishes messages to a Andy X Node. The Andy X Node processes the messages."
lead: "A producer is a process that attaches to a topic and publishes messages to a Andy X Node. The Andy X Node processes the messages."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "concepts-architecture"
weight: 208
toc: true
---

<center><img src="~/../../../../../images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

# Overview

This section gives a high-level overview of how the producer works and an introduction to the configuration settings for tuning.

To see examples of producers written in .NET, refers to these guides. For additional examples, including using of Buildersoft Cloud, refers to Buildersoft Cloud docs.

# Concepts

A producer is a process that attaches to a topic and publishes messages to a Andy X. The Andy X it does the processes like storing and sending to consumers. In other words, A producer is an application that is source of data stream, it generates the message and it publishes into a topic.

Andy Producer is conceptually much simpler than the consumer since it has no need for subscription coordination. A producer maps each message to a topic shard in round-robin by default configuration, but can producer can be configured in the form that based on message key it will be stored to a specific shard in the cluster. Andy X guarantee that all messages with the same non-empty key will be sent to the same shard.

As Andy X is designed in that form as Producers will not wait to create a batch of messages and transmit messages as batch, but it will produce messages as they come one-by-one, the communication between Producers and Andy X is based on Websockets in Binary format. It will not require Authorization foreach message, but only ones when it connects.

**How Andy X stores messages into topic shards?**

If the key is provided, the partitioner will hash the key with murmur2 algorithm and devide it by the number of shards. The results is that the same key is always assigned to the same shard. If the key is not provided, always it will store to the a shard. But, this is just one of the configuration you can do with in a Producer. By default all messages will be stored as round-robin in shards.

Communication between **Shards** is configured in **Andy X Cluster Configuration**, and there can be two communication styles **SYNC** and **ASYNC**, for more check Clustering.


## Send Mode

Producers send messages to brokers synchronously (sync) or asynchronously (async), which are based on the configuration of the Producer. If the client requires **Callback** if the messages has been accepted by the node, this is known as **Synchronously Send Mode**. In the other case if the client doesnot requires **Callback**, the node will accept the message and it will ignore the producer, this is known as **Asynchronously Send Mode**. *Both Send Modes works with two Access Modes*.

## Access Mode

Producers support two Access Modes which are based on Instance type and they are Single and Multiple. 

### Single Access Mode

Only one instance of the Producer can send messages to Andy X, this means that if you deploy your application more than one instance, just one of them will connect to Andy X.

### Multiple Access Mode

More than one instance of the same Producer can send messages to Andy X. Also, different Producers may have more than one instance of it that can send data to Andy X.

> **Access modes**
Access modes of Producer will be configured when the producer will be created to Andy X, you can create producers from Buildersoft Cloud or Andy X Cli.

## Batching

Producers also can produce messages as batch of messages in a single request. The batch size is defined by the maximum number of messages and the maximum publish latency.
In Andy X, batches are tracked and stored as individual messages and not as a single units, this means that the Consumers will consume these messages as individual messages.


## Simple Producer

Below you will find a simple code example how to create a new producer which it requires to create a XClient object

```csharp
var producer = Producer<string, MessageExample>.CreateNewProducer(xClient)
    .ForComponent("streams-examples")
    .AndTopic("source-topic")
    .WithName("first-producer")
    .WithSettings(settings =>
    {
        settings.RequireCallback = false;
    })
    .Build();

await producer.OpenAsync();

var result = await producer.SendAsync($"key", new MessageExample() { Text = "first-message" })
```
