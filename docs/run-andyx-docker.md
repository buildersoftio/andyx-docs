# Set up a standalone Andy X in Docker
For local development and testing, you can run Andy X Node as standalone mode on your machine within a Docker container. 

If you have not installed Docker, download the [Community edition](https://www.docker.com/products/container-runtime) and follow the instructions for your OS.

?> **Andy X in production?**
If you're looking to run a full production Andy X installation, see the Deploying an Andy X instance guide.

## Start Andy X in Docker
> For MacOS, Linux, and Windows:

```sh
    $ docker run -it -p 6540:6540 -e ANDYX_ENVIRONMENT='Development' -e ANDYX_URLS='http://localhost:6540' buildersoftdev/andyx:2.1.0
```
A few things to note about this command:
    
* With this command we are not storing the configurations at all, to persist configurationon Docker volumes in order to not start "fresh" every time the container is restarted. For details on the volumes you can use `docker volume inspect <sourcename>`

```sh
        docker run -it -p 6540:6540 -e ANDYX_ENVIRONMENT='Development' -e ANDYX_URLS='http://localhost:6540' --mount source=andyxconfig,target=/app/config buildersoftdev/andyx:2.1.0
```

* Environment variables like **ANDYX_ENVIRONMENT** is needed to start the Node as Development Environment, **ANDYX_URLS** will explose the node url inside the container.

* For Docker on Windows make sure to configure it to use Linux containers

If you start Andy X successfully, you will see Information-level log messages like this:

```sh
                     Starting Buildersoft Andy X
                     Copyright (C) 2022 Buildersoft LLC
    ###      ###
      ###  ###       Andy X 2.1.0. Copyright (C) 2022 Buildersoft LLC
        ####         Licensed under the Apache License 2.0.  See https://bit.ly/3DqVQbx
      ###  ###
    ###      ###     Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations.

                     Port exposed 6540

                     Starting Buildersoft Andy X Node...


    2022-02-16 22:06:54  andyx  Information      |     Andy X Node is ready
```
?> **Tips**
When you start a local Andy X Node cluster, there are **system**, **default** and **public** tenants created automatically. You can use default and public tenants for development purposes. You can create any product/component and topic within default and public tenants.

## Use Andy X in Docker

Andy X offers client libraries for .NET, Java, Python etc. If you are running a local cluster, you can use the root url to interact with your cluster:
  
  > http://localhost:6540

The following example will guide you get started with Andy X quickly by using Andy X Client for .NET

Add Andy X Client library from Nuget to your app:

    Install-Package Buildersoft.Andy.X.Client -Version 2.1.6
    or
    <PackageReference Include="Buildersoft.Andy.X.Client" Version="2.1.6" />


## Use Andy X Bundle in Docker with docker-compose

Andy X platform has been designed as distributed system. The Node is the edge service that connects Producers and Consumers with eachother, for the design Node do not store messages. To persist messages you will need to deploy **Andy X Storage**.

?> **What is Andy X Storage**
Is an open-source standalone service that is used to store messages for Andy X. The Storage offers support for Multitenancy storage. It hosts all messages and makes sure that all of them are readable for the client. As solution is designed from the begining to be seperate from the Node. Storages can be deployed individually and can connect to the same node. All nodes that connects to a storage are linked with each-other as cluster. It can be configured to store messages in Shard or as Replicas.

!> **More than one storage can be linked with a single node.**

Also, in the Bundle it's great to have the **Andy X Portal** as well. 

?> **What is Andy X Portal**
Is an open-source cloud-native web application designed to manage Andy X Nodes and Storages already deployed. It's a standalone web app that it is used to check Andy X Cluster. As a solutions has been designed from the beginning to be cloud-native also can run on-prem using Docker. Portal can be deployed as standalone application.

We are using docker-compose to run this bundle of services with each-other as a simple cluster.

?> **What is docker-compose**
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
      image: buildersoftdev/andyx-portal:v1.0.0
      ports:
        - 9000:80
      environment:
        - XNode:ServiceUrl=http://andyxnode:6540
      networks:
        - local
# ------------------------------------------------------------------------------------------------

    andyx-storage:
      container_name: andyx-storage
      image: buildersoftdev/andyxstorage:2.1.0
      environment:
        - ANDYX_ENVIRONMENT=Development
        - XNodes__0:ServiceUrl=http://andyxnode:6540
        - XNodes__0:Subscription=1
        - XNodes__0:Username=admin
        - XNodes__0:Password=admin
        - Agent:MaxNumber=16
        - DataStorage:Name=dev-local-01-storage
      volumes:
        - ./data:/app/data
      networks:
        - local
        
# ------------------------------------------------------------------------------------------------
    
    andyx:
      container_name: andyxnode
      image: buildersoftdev/andyx:2.1.0
      ports:
        - 6540:6540
      environment:
        - ANDYX_ENVIRONMENT=Development
        - ANDYX_URLS=http://andyxnode:6540
      volumes:
        - ./xnode_config:/app/config
      networks:
        - local

# ------------------------------------------------------------------------------------------------
  networks:
    local:
      driver: bridge
```

By executing the command to run Andy X Bundle, there will be three containers create like:
- **andyx-portal**
- **andyx-storage**
- **andyxnode**

### What will happen with this docker-compose file?

This is a great question, but if you have some knowledge as DevOps this will be easy-peasy.
In the moment that the containers are up and running, in the same folder with docker-compose file for **andyxnode** container there will be created a **xnode_config** directory with node configurations, this is needed if the contanier dies, next time the container will take the same configuration as it was before.

      volumes:
        - ./xnode_config:/app/config

The same thing is happening with **andyx-storage** container as we are creating a volume to store storage-configuration and data.

      volumes:
        - ./data:/app/data


!> **Andy X Node and Andy X Storage, offers different configurations via Environment Variables, Environment Variables are described in the [Node](nodes-configurations.md) and [Storage](storages-configurations.md) documentation.