---
title: "Configurations"
description: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "nodes"
weight: 302
toc: true
---

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Configuration

Andy X Node can be configured anytime, but these configurations will require restarting on the Node. There are two groups of configurations per each node:

* Storage Configuration,
* Transport Configuration

### Storage Configuration

Default values of Topic related storage configurations can be changed within the config file **data/active/storage_config.json**. In the table bellow are shown the settings you can apply to the node.

| Keys  | Description  | 
| :------------ |:---------------|
| **DefaultWriteBufferSizeInBytes** | *write_buffer_size* sets the size of a *single memtopic*. Once memtopic exceeds this size, it is marked immutable and a new one is created, for now we are creating as **100MB** SIZE.|
| **DefaultMaxWriteBufferNumber** | *max_write_buffer_number* sets the maximum number of memtopics, both active and immutable. If the active memtopic fills up and the total number of memtopics is larger than *max_write_buffer_number* we stall further writes. This may happen if the flush process is slower than the write rate. |
| **DefaultMaxWriteBufferSizeToMaintain** | The amount of write history to maintain in memory, in bytes. This includes the current memtopic size, sealed but unflushed memtopics, and flushed memtopics that are kept around. Andy X will try to keep at least this much history in memory - if dropping a flushed memtopic would result in history falling below this threshold, it would not be dropped. (Default: 0) |
| **DefaultMinWriteBufferNumberToMerge** | *min_write_buffer_number_to_merge* is the minimum number of memtopics to be merged before flushing to storage. For example, if this option is set to 2, immutable memtopics are only flushed when there are two of them - a single immutable memtopic will never be flushed. If multiple memtopics are merged together, less data may be written to storage since two updates are merged to a single key. However, every Get() must traverse all immutable memtopics linearly to check if the key is there. Setting this option too high may hurt read performance. |
| **DefaultMaxBackgroundCompactionsThreads** | *max_background_compactions* is the maximum number of concurrent background compactions. The default is 1, but to fully utilize your CPU and storage you might want to increase this to the minimum of (the number of cores in the system, the disk throughput divided by the average throughput of one compaction thread). |
| **DefaultMaxBackgroundFlushesThreads** | *max_background_flushes* is the maximum number of concurrent flush operations. It is usually good enough to set this to 1. |
| **MaxLogFileSizeInBytes** | *max_log_file_size* file size in bytes for rocksdb logs, *default is 104857600*. |
| **DeleteObsoleteFilesPeriodMilliseconds** | *DeleteObsoleteFilesPeriodMilliseconds* the interval for checking when to delete obsolete files *default is 1800000*. |
| **EnableWriteThreadAdaptiveYield** | *EnableWriteThreadAdaptiveYield* |
| **MaxFileOpeningThreads** | *MaxFileOpeningThreads* number of internal files opening in same time, *default is 4*. |
| **KeepLogFileNumber** | *KeepLogFileNumber* number of keeping log files, *default is 5*. |
| **DumpStatsInSeconds** | *DumpStatsInSeconds* interval of keeping stats in memory, *default is 5*. |
| **ClusterWriteBufferSizeInBytes** | *ClusterWriteBufferSizeInBytes*, *default is 128000000*. |
| **ClusterMaxWriteBufferNumber** | *ClusterMaxWriteBufferNumber*, *default is 4*. |
| **ClusterMaxWriteBufferSizeToMaintain** | *ClusterMaxWriteBufferSizeToMaintain*, *default is 0*. |
| **ClusterMinWriteBufferNumberToMerge** | *ClusterMinWriteBufferNumberToMerge*, *default is 2*. |
| **ClusterMaxBackgroundCompactionsThreads** | *ClusterMaxBackgroundCompactionsThreads*, *default is 2*. |
| **ClusterMaxBackgroundFlushesThreads** | *ClusterMaxBackgroundFlushesThreads*,  *default is 1*. |
| **ClusterMaxBackgroundCompactionsThreads** | *DumpStatsInSeconds* interval of keeping stats in memory, *default is 5*. |
| **InboundMemoryReleaseInMilliseconds** | *InboundMemoryReleaseInMilliseconds* release memory interval if is not being used, *default is 300000*. |
| **InboundFlushCurrentEntryPositionInMilliseconds** | *InboundFlushCurrentEntryPositionInMilliseconds* flushing pointers to disk, *default is 5000*. |
| **OutboundBackgroundIntervalReadMessagesInMilliseconds** | *OutboundBackgroundIntervalReadMessagesInMilliseconds* service checking for new messages after all messages are consumed, *default is 500*. |
| **OutboundFlushCurrentEntryPositionInMilliseconds** | *OutboundFlushCurrentEntryPositionInMilliseconds* flushing pointers to disk, *default is 5000*. |
| **RetentionBackgroundServiceIntervalInMinutes** | *RetentionBackgroundServiceIntervalInMinutes* interval of retention service, *default is 30*. |
| **RetentionBulkMessagesCountToAnalyze** | *RetentionBulkMessagesCountToAnalyze* number of messages to check from retention service, *default is 1000*.|

#### storage_config.json and storage_initial.json

if storage_config.json does exits on **data/active/storage_config.json**, please do configurations in this file. In case, if the node is deployed but not-started changes can be done from **settings/initial_configs/storage_initial.json**.

> **Attention**, if node is running, changes from settings/initial_configs/storage_initial.json will not be submitted.

```json
{
  "KeepLogFileNumber": 5,
  "DumpStatsInSeconds": 5,
  "DeleteObsoleteFilesPeriodMilliseconds": 1800000,
  "EnableWriteThreadAdaptiveYield": true,
  "MaxFileOpeningThreads": 4,
  "MaxLogFileSizeInBytes": 104857600,
  "InboundMemoryReleaseInMilliseconds": 300000,
  "InboundFlushCurrentEntryPositionInMilliseconds": 5000,
  "OutboundFlushCurrentEntryPositionInMilliseconds": 5000,
  "OutboundBackgroundIntervalReadMessagesInMilliseconds": 500,
  "DefaultWriteBufferSizeInBytes": 64000000,
  "DefaultMaxWriteBufferNumber": 4,
  "DefaultMaxWriteBufferSizeToMaintain": 0,
  "DefaultMinWriteBufferNumberToMerge": 2,
  "DefaultMaxBackgroundCompactionsThreads": 1,
  "DefaultMaxBackgroundFlushesThreads": 1,
  "ClusterWriteBufferSizeInBytes": 128000000,
  "ClusterMaxWriteBufferNumber": 4,
  "ClusterMaxWriteBufferSizeToMaintain": 0,
  "ClusterMinWriteBufferNumberToMerge": 2,
  "ClusterMaxBackgroundCompactionsThreads": 2,
  "ClusterMaxBackgroundFlushesThreads": 1,
  "RetentionBackgroundServiceIntervalInMinutes": 30,
  "RetentionBulkMessagesCountToAnalyze": 1000
}
```


### Transport Configuration

Transport configuration can be changed within the config file **data/active/transport_config.json**. In the table bellow are shown the settings you can apply to the node.

| Keys  | Description  | 
| :------------ |:---------------|
| **ClientTimeoutInterval** | *ClientTimeoutInterval* The server considers the client disconnected if it hasn't received a message (including keep-alive) in this interval. It could take longer than this timeout interval for the client to be marked disconnected due to how this is implemented. The recommended value is double the KeepAliveInterval value, default is 30|
| **HandshakeTimeout** | *HandshakeTimeout* If the client doesn't send an initial handshake message within this time interval, the connection is closed. This is an advanced setting that should only be modified if handshake timeout errors are occurring due to severe network latency, default is 15|
| **KeepAliveInterval** | *KeepAliveInterval* If the server hasn't sent a message within this interval, a ping message is sent automatically to keep the connection open. When changing KeepAliveInterval, change the ServerTimeout or serverTimeoutInMilliseconds setting on the client. The recommended **ServerTimeout** or **serverTimeoutInMilliseconds** value is *double the KeepAliveInterval* value, default is 15|
| **StreamBufferCapacity** | *StreamBufferCapacity* The maximum number of items that can be buffered for client upload streams. If this limit is reached, the processing of invocations is blocked until the server processes stream items, default is 10|
| **MaximumReceiveMessageSizeInBytes** | *MaximumReceiveMessageSizeInBytes* Maximum size of a single incoming message, default is un-limited|
| **MaximumParallelInvocationsPerClient** | *MaximumParallelInvocationsPerClient* The maximum number of hub methods that each client can call in parallel before queueing, default is 1|
| **ApplicationMaxBufferSizeInBytes** | *ApplicationMaxBufferSizeInBytes* The maximum number of bytes received from the client that the server buffers before applying backpressure. Increasing this value allows the server to receive larger messages faster without applying backpressure, but can increase memory consumption, default is 64000|
| **TransportMaxBufferSizeInBytes** | *TransportMaxBufferSizeInBytes* The maximum number of bytes sent by the app that the server buffers before observing backpressure. Increasing this value allows the server to buffer larger messages faster without awaiting backpressure, but can increase memory consumption, default is 64000|

#### transport_config.json and transport_initial.json

if transport_config.json does exits on **data/active/transport_config.json**, please do configurations in this file. In case, if the node is deployed but not-started changes can be done from **settings/initial_configs/transport_initial.json**.

> **Attention**, if node is running, changes from settings/initial_configs/transport_initial.json will not be submitted.

```json
{
  "ClientTimeoutInterval": 30,
  "HandshakeTimeout": 15,
  "KeepAliveInterval": 15,
  "StreamBufferCapacity": 10,
  "MaximumReceiveMessageSizeInBytes": null,
  "MaximumParallelInvocationsPerClient": 1,
  "ApplicationMaxBufferSizeInBytes": 64000,
  "TransportMaxBufferSizeInBytes": 64000
}
```