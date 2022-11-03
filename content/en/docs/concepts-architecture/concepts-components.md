---
title: "Components"
description: "A component is a subdomain or a subproduct unit within a product."
lead: "A component is a subdomain or a subproduct unit within a product."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "concepts-architecture"
weight: 206
toc: true
---

<center><img src="~/../../../../../images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Overview

A component is a subdomain or a subproduct unit within a product. The configuration policies set on a component applies to all topics created in that component. A product may create multiple topics via Andy X Cli, self-administration using the REST API or Andy X Clients. For instance, an application with different domains can create a separate components for each application.

Names for topics in the same comonent will look like this:

```
  andyx://{tenant}/{product}/{component}/{topic}
  andyx://tenant/application1/clients/topic-01
  andyx://tenant/application1/clients/topic-02
  andyx://tenant/application1/clients/topic-03
```

## Component 

A component is a subdomain or a subproduct unit within a product. The configuration policies set on a component applies to all topics created in that component.

To each component in a product in an Andy X instance you can assign:

* An authorization schema

When a Component is created in Andy X Cluster inside a Product, all configurations for that component will be replicated to all nodes across Andy X Cluster. As you know already a component have it own authorization schema, Retention Policies and other configurations like the table below.

***Component will inherit all settings from the Product***, but users can set different settings for the component it self, which will *ignore settings* from the **Product**. In case of you would like to expose data from a component to some speficic clients without granting access to entire Product or Tenant.

### Settings

| Settings Keys  | Description  | 
| :------------ |:---------------|
| **IsTopicAutomaticCreationAllowed** | If this property is set, new topics will be able to be created from the client side, if not new topics can be created only from *Andy X Cli* or *Buildersoft Cloud*|
| **IsAuthorizationEnabled** | If this property is set, it will require every client of this component to provide a Component Key and Secret, if not clients will have to provide Product or Tenant Authorization Settings |
| **EnforceSchemaValidation** | If this property is set, nodes will validate schema for each message before storing it |
| **IsSubscriptionAutomaticCreationAllowed** | If this property is set, new subscriptions will be able to be created from the client side, if not new subscriptions can be created only from *Andy X Cli* or *Buildersoft Cloud*|
| **IsProducerAutomaticCreationAllowed** | If this property is set, new producers will be able to be created from the client side, if not new producers can be created only from *Andy X Cli* or *Buildersoft Cloud*|


### Component Retention Policies

Each **Component** in a Product in an Andy X instance can have their own Retention Policies for Message TTL. There can be only two different configurations of TTL which are

* **SOFT_TTL**,
* **HARD_TTL**

**SOFT_TTL**, when the time come to remove a list of messages from the topics, it will check the entries with Subscription logs it these messages where acked from Subscriptions, if not these messages will not be deleted until messages are acked from all Subscriptions created.

**HARD_TTL**, in case of HARD_TTL, it will not check if Subscriptions have acked the messages. Messages will be deleted regardless if the messages are acked or not.

*SOFT_TTL should not have a TTL greater than HARD_TTL*.
For a component, both TTL types can be configurated.

In case if you have **Retention Policy** created in **Tenant**, **Product** and **Component** level. The rules will of executions will be as following.

* Foreach topic in a component with retention policy from Tenant to Component, **only Component Retention Policies will apply**.
* Foreach topic in a component with retention policy from Tenant to Product, **only Product Retention Policies will apply**.
* Foreach topic in a component with retention policy only configured on Tenant level, **only Tenant Retention Policies will apply**.