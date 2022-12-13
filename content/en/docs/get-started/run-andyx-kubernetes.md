---
title: "Run Andy X Kubernetes"
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "get-started"
weight: 104
toc: true
---

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

Kubernetes is an open source container orchestration engine for automating deployment, scaling, and management of containerized applications. The open source project is hosted by the Cloud Native Computing Foundation (CNCF).

# Set up a standalone Andy X in Kubernetes

For local development and testing, you can run Andy X as standalone mode on your machine within a Kubernetes cluster.
You can install Kubernetes engine within Docker Community Edition
If you have not installed Docker, download the [Community edition](https://www.docker.com/products/container-runtime) and follow the instructions for your OS.

If you have not installed any Kubernetes client, download the [tools](https://kubernetes.io/docs/tasks/tools/) and follow the instructions for your OS.

{{< alert icon="Andy X in production?" title="Andy X in production?" text="If you're looking to run a full production Andy X installation, see the Deploying a Andy X instance guide." />}}

## Start Andy X in Kubernetes

To be able to run Andy X on Kubernetes, first you need to create two files ```deploy.yml``` and ```service.yml```.
```deploy.yml``` is known as Deployment object.

A Kubernetes user or administrator specifies data in a YAML file, typically to define a Kubernetes object. The YAML configuration is called a “manifest”, and when it is “applied” to a Kubernetes cluster, Kubernetes creates an object based on the configuration.
A Kubernetes Deployment YAML specifies the configuration for a Deployment object—this is a Kubernetes object that can create and update a set of identical pods. Each pod runs specific containers, which are defined in the spec.template field of the YAML configuration.

### Deployment YAML for Andy X
The following YAML configuration creates a Deployment object that runs 1 replica of Andy X Container.

``` yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: andyx-deployment
  labels:
    app: andyx-node
spec:
  replicas: 1
  selector:
    matchLabels:
      app: andyx-node
  template:
    metadata:
      labels:
        app: andyx-node
    spec:
      containers:
        - name: andyx-node
          image: 'buildersoftdev/andyx:3.0.0'
          imagePullPolicy: Always
          ports:
            - containerPort: 80
          env:
            - name: ANDYX_ENVIRONMENT
              value: Development
            - name: ANDYX_URLS
              value: http://+:80
```

To be able to run and create an Andy X Pod, run the following commad in the folder where you have saved ```deploy.yml``` file.

```
kubectl apply -f deploy.yml
```

After appling the ```deploy.yml``` in Kubernetes you can run the following command to check if your pod has been created

```
kubectl get pods
```

If the result will be like

```

NAME                                READY   STATUS    RESTARTS   AGE
andyx-deployment-86866cb4d4-bgnhr   1/1     Running   0          30m
```

For now the pod has been created, and to check that the service is running inside this pod, run the following command

```
// andyx-deployment-86866cb4d4-bgnhr is the name of the POD, in your case can be different

kubectl logs andyx-deployment-86866cb4d4-bgnhr
```

and result will be as following

```
2022-12-13 14:50:36  andyx   Warning          |     Storing keys in a directory '"/root/.aspnet/DataProtection-Keys"' that may not be persisted outside of the container. Protected data will be unavailable when container is destroyed.
2022-12-13 14:50:36  andyx   Warning          |     No XML encryptor configured. Key {2f268e79-d0bb-47e8-a1bf-0cc79a3ce12a} may be persisted to storage in unencrypted form.
                   Starting Buildersoft Andy X
                   Set your information in motion.

  ###      ###
    ###  ###       Andy X v3.0.0. Developed with (love) by Buildersoft Inc.
      ####         Licensed under the Apache License 2.0. See https://bit.ly/3DqVQbx
    ###  ###
  ###      ###     Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations.

                   Port exposed 80

                   Starting Buildersoft Andy X...


2022-12-13 14:50:36  andyx   Information      |     Starting Buildersoft Andy X...

2022-12-13 14:50:36  andyx   Information      |     Server environment:os.name: Linux
2022-12-13 14:50:36  andyx   Information      |     Server environment:os.platform: Unix
2022-12-13 14:50:36  andyx   Information      |     Server environment:os.version: Unix 5.10.102.1
2022-12-13 14:50:36  andyx   Information      |     Server environment:os.is64bit: True
2022-12-13 14:50:36  andyx   Information      |     Server environment:domain.user.name: andyx-deployment-86866cb4d4-bgnhr
2022-12-13 14:50:36  andyx   Information      |     Server environment:user.name: root
2022-12-13 14:50:36  andyx   Information      |     Server environment:processor.count: 16
2022-12-13 14:50:36  andyx   Information      |     Server environment:dotnet.version: 7.0.0

2022-12-13 14:50:36  andyx   Information      |     Update settings
2022-12-13 14:50:36  andyx   Information      |     Node identifier is 'andyx_standalone'
2022-12-13 14:50:36  andyx   Information      |     Configuration endpoints are exposed
2022-12-13 14:50:37  andyx   Information      |     Starting cluster for the first time
2022-12-13 14:50:37  andyx   Information      |     Initial configuration in process ...
2022-12-13 14:50:37  andyx   Information      |     Initial configuration is done
2022-12-13 14:50:38  andyx   Information      |     Retention service for system/connections/storage/events is initiaized
2022-12-13 14:50:38  andyx   Information      |     Retention service for system/connections/producer/events is initiaized
2022-12-13 14:50:38  andyx   Information      |     Retention service for system/connections/consumer/events is initiaized
2022-12-13 14:50:38  andyx   Information      |     Andy X is ready
```


As you saw, Andy X is running inside a POD, but its unreachable from the client side. In this case you will have to configure the ```service.yml``` configuration file.

### Service YAML for Andy X

Services are how pods communicate in a network environment, either with each other in a Kubernetes cluster or with the outside world. They do this by specifying a port for the caller to use, and a targetPort, which is the port on which the Pod itself receives the message.
Services know which pods to target based on labels specified in the selector.

The following YAML configuration creates a Kubernetes Service object that exposes Andy X Pod.

``` yaml
apiVersion: v1
kind: Service
metadata:
  name: andyx-node
  labels:
    app: andyx-node
spec:
  ports:
    - port: 80
      targetPort: 6540
  selector:
    app: andyx-node
  type: LoadBalancer
  
```

To apply this service configuration, run the following commad in the folder where you have saved ```service.yml``` file.

```
kubectl apply -f service.yml
```

After appling the ```service.yml``` in Kubernetes you can run the following command to check if you have exposed Andy X Pod

```
kubectl get service
```

and the result will be like

```
NAME         TYPE           CLUSTER-IP       EXTERNAL-IP   PORT(S)        AGE
andyx-node   LoadBalancer   10.110.250.245   localhost     80:31600/TCP   52m
kubernetes   ClusterIP      10.96.0.1        <none>        443/TCP        70m
```

<p> <strong>Andy X offers different configurations via Environment Variables, Environment Variables are described in the <a href="/docs/nodes/configurations/" role="">Node</a> documentation.</strong></p>