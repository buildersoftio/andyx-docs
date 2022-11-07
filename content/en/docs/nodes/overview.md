---
title: "Overview"
description: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "nodes"
weight: 301
toc: true
---

<center><img src="~/../../../../../images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Overview
The bridge that connects clients with each-other (Producers and Consumers) is Node service. An Andy X Node also known as Broker. A single Andy X Server is called a Andy X Node. That Andy X Node is a program that runs on the .NET eco-system (on top of CLR) and usally a server that is meant to be an Andy X Node will solely run the necessary program and nothing else. Nodes can connect with each-other to create a Cluster.

In the diagram bellow, are shown all the internal components of Andy X Node.
<center><img src="~/../../../../../images/andyx-node-high.png" style="margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Endpoints

Endpoints or Public API that are exposed with Andy X Node are described bellow.

### Admin Rest Endpoints

Administration APIs or also known as Admin Rest Endpoints within Andy X Node helps users to manage the state of the Server, like managing Tenants, Products, Components, Topics, Retention Policies, Subscriptions, Consumers and Producers. 

Andy X Cli and Andy X Portal are powered by these endpoints. By default these endpoints are exposed, but also Sys Admins can de-expose by setting the envirnment variable '**ANDYX_EXPOSE_CONFIG_ENDPOINTS**' to false.

### Cluster BinaryAPI

Andy X Node also offers Cluster BinaryAPIs which enables to communicate between nodes inside a cluster. Andy X Cluster offers two types of nodes, distributed and replicas. These Endpoints transmits also Admin changes from a Node to others. *e.g., If a retention policy is created in a Node, that retention will be replicated to all nodes inside the cluster.* 
> Cluster BinaryAPI can be used only from Nodes internally.

### Producer BinaryAPI

**Producer BinaryAPIs** are developed to enable communication between Producers and the Server. These endpoints are being used anytime that a Message is send to the Server. Producer BinaryAPIs are async endpoints, which the server can notify the Producer when the message is accepted or other events.

### Consumer BinaryAPI

**Consumer BinaryAPIs** are developed to enable communication between Server and Consumer. These endpoints are being used from the Andy X Client libraries.