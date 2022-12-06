---
title: "Tenants"
description: "Andy X was created from the ground up as a multi-tenant system.To support multi-tenancy, Andy X has a concept of tenants."
lead: "Andy X was created from the ground up as a multi-tenant system.To support multi-tenancy, Andy X has a concept of tenants."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "concepts-architecture"
weight: 204
toc: true
---

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Overview

<p>Andy X was created from the ground up as a multi-tenant system.To support multi-tenancy, Andy X has a concept of tenants. Tenants can be spread across nodes in a Cluster and can each have their own <a href="/docs/security/overview/" role="">authentication and authorization</a> scheme applied to them. They are also the administrative unit at which storage quotas, message TTL, and isolation policies can be managed.</p>

## Tenants

To each tenant in an Andy X instance you can assign:

* **An authorization schema**
* **The set of clusters to which the tenant's configuration applies (only for Buildersoft Cloud)**

When a Tenant is created in Andy X Cluster, all configurations for that tenant will be replicated to all nodes across Andy X Cluster.
As you know already a tenant have it own authorization schema, Retention Policies and other configurations like

### Settings

| Settings Keys  | Description  | 
| :------------ |:---------------|
| **IsProductAutomaticCreationAllowed** | If this property is set, products will be able to be created from the client side, if not products can be created only from *Andy X Cli* or *Buildersoft Cloud*|
| **IsEncryptionEnabled** | If this property is set, it will encrypt messages inside this tenant, and it will require to add an encryption key |
| **IsAuthorizationEnabled** | If this property is set, it will require every client of this tenant to provide a Tenant Key and Secret, if not clients can connect freely |

Also, there is another setting property which can activate or deactivate a tenant. 

### Tenant Retention Policies

Each tenant in an Andy X instance can have their own Retention Policies for Message TTL. There can be only two different configurations of TTL which are

* **SOFT_TTL**,
* **HARD_TTL**

**SOFT_TTL**, when the time come to remove a list of messages from the topics, it will check the entries with Subscription logs it these messages where acked from Subscriptions, if not these messages will not be deleted until messages are acked from all Subscriptions created.

**HARD_TTL**, in case of HARD_TTL, it will not check if Subscriptions have acked the messages. Messages will be deleted regardless if the messages are acked or not.

*SOFT_TTL should not have a TTL greater than HARD_TTL*.
For a tenant, both TTL types can be configurated.