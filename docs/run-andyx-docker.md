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
