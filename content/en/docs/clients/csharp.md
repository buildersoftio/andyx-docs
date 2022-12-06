---
title: "C#"
description: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
lead: "Andy X is an open-source distributed streaming platform designed to deliver the best performance possible for high-performance data pipelines, streaming analytics, streaming between microservices and data integrations."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "clients"
weight: 602
toc: true
---

<center><img src="/images/T1.png" style="height:100px; margin-top: 40px; margin-bottom: 40px" alt="andy x logo" align="middle"></center>

You can use the Andy X C# Client (Buildersoft.Andy.X.Client) to create Andy X Producers and Consumers. This client supports all feature of Andy X v3.

All methods in the Producer and Consumer are thread-safe.

## Installation

This section describes how to install the Andy X for .NET client library through the dotnet CLI.

Alternatively, you can install the Andy X for .NET client library through Visual Studio. Note that starting from Visual Studio 2017, the dotnet CLI is automatically installed with any .NET Core related workloads. For more information, see [Microsoft documentation](https://learn.microsoft.com/en-us/visualstudio/mac/nuget-walkthrough?view=vsmac-2019).

To install the Andy X for .NET client library using the dotnet CLI, follow these steps:

  1. Install the [.NET SDK](https://dotnet.microsoft.com/en-us/download), which provides the dotnet CLI.
  2. Create a project.
     1. Create a folder for the project.
     2. Open a terminal window and switch to the new folder.
     3. Create the project using the following command.
     
     ```
     dotnet new console
     ```

     4. Use ```dotnet run``` to test that the app has been created properly.
  3. Add the Buildersoft.Andy.X.Client Nuget Package.
     1. Use the following command to install the ```Buildersoft.Andy.X.Client``` package.
     
     ```
     dotnet add package Buildersoft.Andy.X.Client
     ```

     2. After the command completes, open the .csproj file to see the added reference.

     ``` xml
     <ItemGroup>
        <PackageReference Include="Buildersoft.Andy.X.Client" Version="3.0.0" />
     </ItemGroup>
     ```

## Connectivity

To connect to Andy X using this library, first you need to specify ServiceUrl of the Node where Andy X is deployed.

You can assign Andy X Node ServiceUrl of an Andy X Cluster. The following is an example of ```localhost``` with the default port ```6540```:

```
http://localhost:6540
```

If you use SSL certs use
```
https://localhost:6541
```

## Client

This section describes some configuration examples for the Andy X for .NET client.

### Create Client

This example shows how to create a Andy X for .NET client connected to localhost.

```csharp
using Andy.X.Client;

var xClient = XClient.CreateClient()
      .ForService(new Uri("http://localhost:6540"))
      .AndTenant("default")
      .AndProduct("product")
      .Build();
```

To create an Andy X Client by using the CreateClient Builder, you can add settings parameters like the example bellow.

```csharp
using Andy.X.Client;

var xClient = XClient.CreateClient()
      .ForService(new Uri("http://localhost:6540"))
      .AndTenant("default")
      .AndProduct("product")
      .WithSettings(settings =>
      {
          settings.EnableAutoReconnect = true;
      })
      .Build();
```

### Create Producer

This section describes how to create a producer.

Create a producer by using the producer builder.

```csharp
using Andy.X.Client;
using Andy.X.Client.Abstractions.Producers;

IProducer<string, byte[]> producer = Producer<string, byte[]>.CreateNewProducer(xClient)
    .ForComponent("my-component")
    .AndTopic("my-topic")
    .WithName("my-producer")
    .Build();

await producer.OpenAsync();
```

Create a producer by using the producer builder with settings.

```csharp
using Andy.X.Client;
using Andy.X.Client.Abstractions.Producers;


IProducer<string, byte[]> producer = Producer<string, byte[]>.CreateNewProducer(xClient)
    .ForComponent("my-component")
    .AndTopic("my-topic")
    .WithName("my-producer")
    .WithSettings(settings =>
    {
        settings.RequireCallback = false;
    })
    .Build();

await producer.OpenAsync();
```

### Create Consumer

This section describes how to create a consumer.

Create a consumer by using the consumer builder.

```csharp
using Andy.X.Client;
using Andy.X.Client.Abstractions.Consumers;

IConsumer<string, NotificationReceived> consumer = Consumer<string, NotificationReceived>.CreateNewConsumer(xClient)
    .ForComponent("my-component")
    .AndTopic("my-topic")
    .WithName("my-consumer")
    .AndSubscription(subscription =>
    {
        subscription.Name = "my-subscription";
        subscription.Type = SubscriptionType.Unique;
        subscription.Mode = SubscriptionMode.NonResilient;
        subscription.InitialPosition = InitialPosition.Earliest;
    })
    .Build();
```


Create a consumer by using the consumer builder with settings.

```csharp
using Andy.X.Client;
using Andy.X.Client.Abstractions.Consumers;

IConsumer<string, NotificationReceived> consumer = Consumer<string, NotificationReceived>.CreateNewConsumer(xClient)
    .ForComponent("my-component")
    .AndTopic("my-topic")
    .WithName("my-consumer")
    .AndSubscription(subscription =>
    {
        subscription.Name = "my-subscription";
        subscription.Type = SubscriptionType.Unique;
        subscription.Mode = SubscriptionMode.NonResilient;
        subscription.InitialPosition = InitialPosition.Earliest;
    })
    .WithSettings(settings =>
    {
        settings.CompressionType = CompressionType.None;
    })
    .Build();
```


## Producer

A producer is a process that attaches to a topic and publishes messages to an Andy X Node for processing. This section describes some configuration examples of the producer.

### Send message

This example shows how to send data.

``` csharp
var data = Encoding.UTF8.GetBytes("Hello World from Andy X");
await producer.SendAsync($"my-key", data);
```

### Send message with customized headers

``` csharp
var data = Encoding.UTF8.GetBytes("Hello World from Andy X");
var headers = new Dictionary<string, string>();
headers.Add("key", "value");
await producer.SendAsync($"my-key", data, headers);
```


## Consumer

A consumer is a process that attaches to a topic through a subscription and then receives messages. This section describes some configuration examples about the consumer.

### Receive messages

This example shows how a consumer receives messages from a topic.

``` csharp
consumer.MessageReceivedHandler((key, message) =>
{
    Console.WriteLine($"message received, {Encoding.UTF8.GetString(message.Payload)}");
    consumer.AcknowledgeMessage(message);
});
await consumer.SubscribeAsync();
```

### Acknowledge messages

Attached to a subscripton there are three forms of Message Acknoledgement
```Acknoledged```, ```Unacknoledged``` and ```Skipped```, and you attach it in the ```MessageReceivedHandler```

``` csharp
  consumer.AcknowledgeMessage(message);
  consumer.SkipMessage(message);
  consumer.UnacknowledgeMessage(message);
```