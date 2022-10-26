---
title: "Topics"
description: "Andy X topics are the categories used to organize messages. Each topic has a name that is unique inside a Component in Andy X Cluster"
lead: "Andy X topics are the categories used to organize messages. Each topic has a name that is unique inside a Component in Andy X Cluster."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "concepts-architecture"
weight: 207
toc: true
---

<center><img src="~/../../../../../images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Overview

This section gives a high-level overview of how the topics works and an introduction to the configuration topic settings for tuning.

To see examples how to create and configure a topic, refers to these guides. For additional examples, including using of Buildersoft Cloud, refers to Buildersoft Cloud docs.

<center><img src="~/../../../../../images/andyx-topic.png" style=" margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Concepts

When an event stream enters Andy X, it is persisted as a topic. In Andy X’s universe, a topic is a materialized event stream. In other words, a topic is a stream at rest.
As in other pub-sub systems, topics in Andy X are named channels for transmitting messages from producers to consumers. Topic names well defined and are stored inside the Tenant/Product/Component/**Topic**

    e.g,
    {tenant}/{Product}/{Component}/{Topic}
    default/transactions/application/txn-received

Andy X topics are the categories used to organize messages. Each topic has a name that is unique inside a Component in Andy X Cluster.
Messages are sent to and read from specific topics.  In other words, producers write data to topics, and consumers read data from topics.
Andy X topics are multi-subscriber.  This means that a topic can have zero, one, or multiple subscriptions to that topic and the data written to it.

In Andy, topics are sharded and replicated across nodes (depends on Cluster Configuration) throughout the implementation. Nodes refers to each of the Main Nodes in Andy X Cluster. Shards are important because they enable parallelization of topics, enabling high message throughput. Below, is illustrating how a topic is created in Andy X Cluster.

<center><img src="~/../../../../../images/high-level-topic.png" style=" margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>
Entries (Offsets) are assigned to each message in a shard to keep track of the messages in the different shards of a topic


## Configuration