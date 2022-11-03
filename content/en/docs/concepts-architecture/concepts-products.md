---
title: "Products"
description: "A Product is the administrative unit nomenclature within a tenant."
lead: "A Product is the administrative unit nomenclature within a tenant."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "concepts-architecture"
weight: 205
toc: true
---

<center><img src="~/../../../../../images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

## Overview

Tenants and product are two key concepts of Andy X to support multi-tenancy.

* Andy X  is provisioned for specified tenants with appropriate capacity allocated to the tenant.
* A Product is the administrative unit nomenclature within a tenant. The configuration policies set on a product apply to all the components/topics created in that product. A tenant may create multiple products via Andy X Cli or self-administration using the REST API. For instance, a tenant with different applications can create a separate products for each application.

Names for topics in the same product will look like this:

```
  andyx://{tenant}/{product}/{component}/{topic}
  andyx://tenant/application1/component/topic-01
  andyx://tenant/application1/component/topic-02
  andyx://tenant/application1/component/topic-03
```

## Product

A Product is the administrative unit nomenclature within a tenant. The configuration policies set on a product apply to all the components/topics created in that product. A tenant may create multiple products via Andy X Cli or self-administration using the REST API.

To each product in a tenant in an Andy X instance you can assign:

* **An authorization schema**
* **The set of clusters to which the product's configuration applies (only for Buildersoft Cloud)**

When a Product is created in Andy X Cluster inside a Tenant, all configurations for that product will be replicated to all nodes across Andy X Cluster. As you know already a product have it own authorization schema, Retention Policies and other configurations like the table below.

***Product will inherit all settings from the Tenant***, but users can set different settings for the product it self, which will *ignore settings* from the **Tenant**. In case of you would like to expose data from a product to some speficic clients without granting access to entire Tenant.

### Settings

| Settings Keys  | Description  | 
| :------------ |:---------------|
| **IsComponentAutomaticCreationAllowed** | If this property is set, components will be able to be created from the client side, if not components can be created only from *Andy X Cli* or *Buildersoft Cloud*|
| **IsAuthorizationEnabled** | If this property is set, it will require every client of this product to provide a Product Key and Secret, if not clients will have to provide Tenant Authorization Settings |


### Product Retention Policies

Each **Product** in a Tenant in an Andy X instance can have their own Retention Policies for Message TTL. There can be only two different configurations of TTL which are

* **SOFT_TTL**,
* **HARD_TTL**

**SOFT_TTL**, when the time come to remove a list of messages from the topics, it will check the entries with Subscription logs it these messages where acked from Subscriptions, if not these messages will not be deleted until messages are acked from all Subscriptions created.

**HARD_TTL**, in case of HARD_TTL, it will not check if Subscriptions have acked the messages. Messages will be deleted regardless if the messages are acked or not.

*SOFT_TTL should not have a TTL greater than HARD_TTL*.
For a product, both TTL types can be configurated.


## Data Mesh and Data Products

The idea behind introducing Products in Andy X, it was the rise of Data Mesh concept.

> Data mesh is an architectural pattern for implementing enterprise data platforms in large, complex organizations. It helps scale analytics adoption beyond a single platform and a single implementation team.

### Data Products
The data as a product archetype is an integral component of a data mesh architecture, and it’s essential for making data governance more scalable across broad parts of a company. Treating data as a product means bringing product thinking to data management, already a common practice in software product development.
**A data product is a reusable data asset, built to deliver a trusted dataset, for more than one specific purpose.**
It collects data from relevant data sources — including raw data — processes it, ensures data quality, and makes it accessible and understandable to anyone who needs it to meet specific needs. Data products are analyzed by data scientists and analysts to inform predictive analytics, build data models, build new reports, assist in machine learning, and more.

A data product makes a dataset easier to understand, easier to discover, and easier to access as a data asset. It generally corresponds to one or more business entities — customers, orders, etc. — and is made up of metadata and dataset instances.

> *Bringing **Data Products** and implementing it at the core of **Andy X**, it will help organizations to adopt a **data mesh** approach to data management. Build high-quality data products see improved efficiency, collaboration, and data democratization. Product or data teams are generally better informed as to the value and end-use of data in real-time world.*

Teams that use data products spend less time searching for data, ensuring data quality, or building new data pipelines, and those time savings become significant when added up across your data ecosystem and lifecycle.

Additionally, data products speed time to insight because they can be reused and repurposed, increase trust in your organizations’ data, and provide real-time data for in-the-moment decision-making.
