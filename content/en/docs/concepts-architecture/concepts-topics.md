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

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Overview

This section gives a high-level overview of how the topics works and an introduction to the configuration topic settings for tuning.

To see examples how to create and configure a topic, refers to these guides. For additional examples, including using of Buildersoft Cloud, refers to Buildersoft Cloud docs.

<center><img src="/images/andyx-topic.png" style=" margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Concepts

When an event stream enters Andy X, it is persisted as a topic. In Andy X’s universe, a topic is a materialized event stream. In other words, a topic is a stream at rest.
As in other pub-sub systems, topics in Andy X are named channels for transmitting messages from producers to consumers. Topic names well defined and are stored inside the Tenant/Product/Component/**Topic**
```
    e.g,
    {tenant}/{Product}/{Component}/{Topic}
    default/transactions/application/txn-received
```

Andy X topics are the categories used to organize messages. Each topic has a name that is unique inside a Component in Andy X Cluster.
Messages are sent to and read from specific topics.  In other words, producers write data to topics, and consumers read data from topics.
Andy X topics are multi-subscriber.  This means that a topic can have zero, one, or multiple subscriptions to that topic and the data written to it.

In Andy, topics are sharded and replicated across nodes (depends on Cluster Configuration) throughout the implementation. Nodes refers to each of the Main Nodes in Andy X Cluster. Shards are important because they enable parallelization of topics, enabling high message throughput. Below, is illustrating how a topic is created in Andy X Cluster.

<center><img src="/images/high-level-topic.png" style=" margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>
Entries (Offsets) are assigned to each message in a shard to keep track of the messages in the different shards of a topic


## Topic

Andy X was built with highly scalable persistent storage of message data as a primary objective. Topics enable you to persistently store as many messages as you need while preserving message ordering. By default, Andy X stores *all* messages produced to a topic.

### Storage Configurations

Topics can have different configurations on the storage level. These configurations should appled for each use-case you may have, e.g., There should be different configurations for a topic that stores billion of messages for day, from the topic has has thousand of messages for day. In the table bellow are shown the settings you can apply to a topic.

| Keys  | Description  | 
| :------------ |:---------------|
| **WriteBufferSizeInBytes** | *write_buffer_size* sets the size of a *single memtopic*. Once memtopic exceeds this size, it is marked immutable and a new one is created, for now we are creating as **100MB** SIZE.|
| **MaxWriteBufferNumber** | *max_write_buffer_number* sets the maximum number of memtopics, both active and immutable. If the active memtopic fills up and the total number of memtopics is larger than *max_write_buffer_number* we stall further writes. This may happen if the flush process is slower than the write rate. |
| **MaxWriteBufferSizeToMaintain** | The amount of write history to maintain in memory, in bytes. This includes the current memtopic size, sealed but unflushed memtopics, and flushed memtopics that are kept around. Andy X will try to keep at least this much history in memory - if dropping a flushed memtopic would result in history falling below this threshold, it would not be dropped. (Default: 0) |
| **MinWriteBufferNumberToMerge** | *min_write_buffer_number_to_merge* is the minimum number of memtopics to be merged before flushing to storage. For example, if this option is set to 2, immutable memtopics are only flushed when there are two of them - a single immutable memtopic will never be flushed. If multiple memtopics are merged together, less data may be written to storage since two updates are merged to a single key. However, every Get() must traverse all immutable memtopics linearly to check if the key is there. Setting this option too high may hurt read performance. |
| **MaxBackgroundCompactionsThreads** | *max_background_compactions* is the maximum number of concurrent background compactions. The default is 1, but to fully utilize your CPU and storage you might want to increase this to the minimum of (the number of cores in the system, the disk throughput divided by the average throughput of one compaction thread). |
| **MaxBackgroundFlushesThreads** | *max_background_flushes* is the maximum number of concurrent flush operations. It is usually good enough to set this to 1. |


> **MemTopic** (aka. Memory Topic) is an **in-memory data structure** holding data before they are flushed to SST files. It serves both read and write - new writes always insert data to memtopic, and reads has to query memtopic before reading from SST files, because data in memtopic is newer. Once a memtopic is full, it becomes immutable and replaced by a new memtopic. A background thread will flush the content of the memtopic into a SST file, after which the memtopic can be destroyed.


Default values for each config key is

| Keys  | Default |
| :------------ |:---------------|
| **WriteBufferSizeInBytes** | 100000000 Bytes (100MB) |
| **MaxWriteBufferNumber** | 4 |
| **MaxWriteBufferSizeToMaintain** | 0 |
| **MinWriteBufferNumberToMerge** | 2 |
| **MaxBackgroundCompactionsThreads** | 1 |
| **MaxBackgroundFlushesThreads** | 1 |


When a new **topic** is created, default configuration values will be passed to that topic from the table above. But, this does not mean that will be always the same, as you can configure default values in **storage_config.json** at

    ~/data/active/storage_config.json


Default topic settings for storage.
```json
{
  "DefaultWriteBufferSizeInBytes": 100000000,
  "DefaultMaxWriteBufferNumber": 4,
  "DefaultMaxWriteBufferSizeToMaintain": 0,
  "DefaultMinWriteBufferNumberToMerge": 2,
  "DefaultMaxBackgroundCompactionsThreads": 1,
  "DefaultMaxBackgroundFlushesThreads": 1,
}
```

### Transport Configuration

Same as Storage Configuration for topic. Also, **Transport Layer** is important for different use-cases you may have. The only drawback for the transport layer is that if you change configuration it will be applied for all topics connected in the node. In the table below are shown the transport configuration.

| Keys  | Description |
| :------------ |:---------------|
| **StreamBufferCapacity** | The maximum number of messages that can be buffered for client upload streams. If this limit is reached, the processing of invocations is blocked until Andy X processes stream messages. |
| **MaximumParallelInvocationsPerClient** | The maximum number of message transmit calls that each client can call in parallel before queueing. |
| **MaximumReceiveMessageSizeInBytes** | Maximum size of a message. Increasing the value may increase the risk of [Denial of service (DoS) attacks](https://developer.mozilla.org/en-US/docs/Glossary/DOS_attack) |
| **ApplicationMaxBufferSizeInBytes** | The maximum number of bytes received from the client that Andy X buffers before applying backpressure. Increasing this value allows the Andy X to receive larger messages faster without applying backpressure, but can increase memory consumption. |
| **TransportMaxBufferSizeInBytes** | The maximum number of bytes sent by the app that Andy X buffers before observing backpressure. Increasing this value allows Andy X to buffer larger messages faster without awaiting backpressure, but can increase memory consumption. |


Default values for each config key is

| Keys  | Default Value |
| :------------ |:---------------|
| StreamBufferCapacity | 10 |
| MaximumParallelInvocationsPerClient | 1 |
| MaximumReceiveMessageSizeInBytes | NO_SOFT_LIMIT,  3GB HARD_LIMIT |
| ApplicationMaxBufferSizeInBytes | 64000 Bytes (64KB) |
| TransportMaxBufferSizeInBytes | 64000 Bytes (64KB) |

Transport Configuration can be configured in transport_config.json config file at

    ~/data/active/transport_config.json

> ***Changing Transport Configurations, it will require to restart the cluster.***