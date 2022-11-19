---
title: "Clusters"
description: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "nodes"
weight: 303
toc: true
---

<center><img src="~/../../../../../images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

Everything related to Andy X runs under an Andy X Cluster. Clusters, in turn, consist of:

* One or more Andy X Nodes (Brokers),
* Custom Rafting quorum used for cluster-level configuration and coordination,
* Cluster Load Balancer (which can be deployed together with nodes, by defaul is pre-confured within Buildersoft Cloud)

Clusters can be configured in three configurations

* **Distributed Nodes** (also knows as Shards),
* **Replicated Nodes** (also knows as Replicas),
* **Production Nodes** a combination of shards and replicas, each main shard can have multiple replicas (it depends on the number of replicas).

<p>To learn more about Clustering, see the  <a href="/docs/clustering/overview/" role="">Clustering</a> guide.</p>

## Metadata store
The Andy X metadata store all the metadata of an Andy X cluster, such as tenant, product, component, topic metadata, node load data, and so on. An*dy X will replicate all metadatas to all nodes connected*. Andy X uses **Andy X Raft** for metadata storage, cluster configuration and coordination. The Andy X Metadata store is bounded inside the Andy X Cluster because of the custom rafting, but in next versions of Andy X, *Metadata store will be able to deploy in a separate service*.

> Andy X with v3.1 will support more metadata backend services, including [FASTER](https://microsoft.github.io/FASTER/), [MSSQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2019), [REDIS](https://redis.io/) and more.

## Persistent storage

Andy x provides guaranteed message delivery for applications. If a message successfully reaches a Andy X node, it will be delivered to its intended target.

This guarantee requires that Andy X will store messages into Topic store (in-memory and disk combination) in a durable manner until they can be delivered to and acknowledged by consumers. This mode of messaging is commonly called *persistent messaging*. In Andy X, based on the Cluster configuration the message will be stored and synced on disk. for example, if there are 2 distributed nodes, 4 messages will go 2 in first node, and the rest in the last node. After messages are stored in main nodes, they will be replicated into replicated nodes.

Andy X uses a system called RocksDb for persistent message storage. RocksDb is embedded [write-ahead log](https://en.wikipedia.org/wiki/Write-ahead_logging) (WAL) system that provides a lot of different configurations.