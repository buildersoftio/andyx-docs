---
title: "Run Andy X Docker"
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "get-started"
weight: 103
toc: true
---

<center><img src="~/../../../../../images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

# Set up a standalone Andy X in Docker
For local development and testing, you can run Andy X Node as standalone mode on your machine within a Docker container.

If you have not installed Docker, download the [Community edition](https://www.docker.com/products/container-runtime) and follow the instructions for your OS.


{{< alert icon="Andy X in production?" title="Andy X in production?" text="If you're looking to run a full production Andy X installation, see the Deploying a Andy X instance guide." />}}

## Start Andy X in Docker
> For MacOS, Linux, and Windows:

```sh
    $ docker run -it -p 6540:6540 -e ANDYX_ENVIRONMENT='Development' -e ANDYX_URLS='http://localhost:6540' buildersoftdev/andyx:3.0.0
```
A few things to note about this command:
    
* With this command we are not storing the configurations at all, to persist configurationon Docker volumes in order to not start "fresh" every time the container is restarted. For details on the volumes you can use `docker volume inspect <sourcename>`

```sh
        docker run -it -p 6540:6540 -e ANDYX_ENVIRONMENT='Development' -e ANDYX_URLS='http://localhost:6540' --mount source=storage,target=/app/data buildersoftdev/andyx:3.0.0
```

* Environment variables like **ANDYX_ENVIRONMENT** is needed to start the Node as Development Environment, **ANDYX_URLS** will explose the node url inside the container.

* For Docker on Windows make sure to configure it to use Linux containers

If you start Andy X successfully, you will see Information-level log messages like this:

```sh
                   Starting Buildersoft Andy X
                   Set your information in motion.

  ###      ###
    ###  ###       Andy X v3.0.0. Developed with (love) by Buildersoft Inc.
      ####         Licensed under the Apache License 2.0. See https://bit.ly/3DqVQbx
    ###  ###
  ###      ###     Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations.

                   Port exposed 6541 SSL
                   Port exposed 6540

                   Starting Buildersoft Andy X...


2022-10-24 00:01:39  andyx   Information      |     Starting Buildersoft Andy X...
2022-10-24 00:01:39  andyx   Information      |     Update settings
2022-10-24 00:01:39  andyx   Information      |     Node identifier is 'andyx_standalone'
2022-10-24 00:01:39  andyx   Information      |     Configuration endpoints are exposed
2022-10-24 00:01:40  andyx   Information      |     Starting cluster for the first time
2022-10-24 00:01:40  andyx   Information      |     Initial configuration in process ...
2022-10-24 00:01:41  andyx   Information      |     Initial configuration is done
2022-10-24 00:01:41  andyx   Information      |     Background service for retention at system/connections/storage/events has been initiaized
2022-10-24 00:01:41  andyx   Information      |     Background service for retention at system/connections/producer/events has been initiaized
2022-10-24 00:01:41  andyx   Information      |     Background service for retention at system/connections/consumer/events has been initiaized
2022-10-24 00:01:41  andyx   Information      |     Andy X is ready
```

{{< alert icon="👉 Tips"  text="When you start a local Andy X Node cluster, there are **system**, **default** and **public** tenants created automatically. You can use default and public tenants for development purposes. You can create any product/component and topic within default and public tenants." />}}

## Use Andy X in Docker

Andy X offers client libraries for .NET, Java, Python etc. If you are running a local cluster, you can use the root url to interact with your cluster:
  
  > http://localhost:6540 or https://localhost:6541

The following example will guide you get started with Andy X quickly by using Andy X Client for .NET

Add Andy X Client library from Nuget to your app:

    Install-Package Buildersoft.Andy.X.Client -Version 3.0.0
    or
    <PackageReference Include="Buildersoft.Andy.X.Client" Version="3.0.0" />


## Use Andy X Bundle in Docker with docker-compose

Andy X platform has been designed as distributed system. The Node is the edge service that connects Producers and Consumers with each-other, you can integrate also other services with Andy X, like **Andy X Portal** and **Andy X Connect** connectors.


> **What is Andy X Portal**
Is an open-source cloud-native web application designed to manage Andy X Nodes and Storages already deployed. It's a standalone web app that it is used to check Andy X Cluster. As a solutions has been designed from the beginning to be cloud-native also can run on-prem using Docker. Portal can be deployed as standalone application.

We are using docker-compose to run this bundle of services with each-other as a simple cluster.

> **What is docker-compose**
Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration. To learn more about all the features of Compose, see the list of features.

To run a docker-compose file we will run the command via terminal in the docker-compose.yaml file.
 
     docker-compose up -d

Below you will find a simple docker-compose file for Andy X Bundle.

```yml
# ------------------------------------------------------------------------------------------------
  version: '3'
# ------------------------------------------------------------------------------------------------
  services:

    andyx-portal:
      container_name: andyx-portal
      image: buildersoftdev/andyx-portal:v3.0.0
      ports:
        - 9000:80
      environment:
        - XNode:ServiceUrl=http://andyx:6540
      networks:
        - local
# ------------------------------------------------------------------------------------------------
    
    andyx:
      container_name: andyx
      image: buildersoftdev/andyx:3.0.0
      ports:
        - 6540:6540
      environment:
        - ANDYX_ENVIRONMENT=Development
        - ANDYX_URLS=http://andyx:6540
      volumes:
        - ./data:/app/data
      networks:
        - local

# ------------------------------------------------------------------------------------------------
  networks:
    local:
      driver: bridge
```

By executing the command to run Andy X Bundle, there will be two containers create like:
- **andyx-portal**
- **andyx**

### What will happen with this docker-compose file?

This is a great question, but if you have some knowledge as DevOps this will be easy-peasy.
In the moment that the containers are up and running, in the same folder with docker-compose file for **andyx** container there will be created a **data** directory with andy x storage, this is needed if the contanier dies, next time the container will take and use the same persistent data and configuration as it was before.

      volumes:
        - ./data:/app/data

Also, like how we started in the second example, we mounted a volume in Docker for Windows. We can also apply the same line in docker-compose

      volumes:
        - andyxdata:/app/data


<p> <strong>Andy X offers different configurations via Environment Variables, Environment Variables are described in the <a href="/docs/nodes/configurations/" role="">Node</a> documentation.</strong></p>