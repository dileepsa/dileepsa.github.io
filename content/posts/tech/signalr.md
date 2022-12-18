---
title: "SignalR"
date: 2022-11-22T23:19:54+05:30
draft: false
Tags: ["Tech"]
---

## What is SignalR?

SignalR is a library for ASP.NET developers that simplifies the process of adding real-time web functionality to applications. Real-time web functionality is the ability to have server code push content to connected clients instantly as it becomes available, rather than having the server wait for a client to request new data.

SignalR provides a simple API for creating server-to-client remote procedure calls (RPC) that call JavaScript functions in client browsers (and other client platforms) from server-side .NET code. SignalR also includes API for connection management (for instance, connect and disconnect events), and grouping connections.

The simple RPC is explained in below image:
![Communication](/images/signalr/signalr_communication.webp)

SignalR supports "server push" functionality, in which server code can call out to client code in the browser using Remote Procedure Calls (RPC), rather than the request-response model common on the web today.

## SignalR Clients

Currently, I am using signalR client using signalrcore module.

Here is the link to the module: [https://pypi.org/project/signalrcore/]()

We can create different clients using javascript,python, Java, c# etc...

## Hubs

A Hub is a more high-level pipeline built upon the Connection API that allows your client and server to call methods on each other directly. SignalR handles the dispatching across machine boundaries as if by magic, allowing clients to call methods on the server as easily as local methods, and vice versa.

## How Hubs work

When server-side code calls a method on the client, a packet is sent across the active transport that contains the name and parameters of the method to be called (when an object is sent as a method parameter, it is serialized using JSON). The client then matches the method name to methods defined in client-side code. If there is a match, the client method will be executed using the deserialized parameter data.

## Configure SignalR hubs

``` c#
var builder = WebApplication.CreateBuilder(args);

builder.Services.AddSignalR();
```

## Creating Hubs

``` c#

public class BikesHub : Hub
{
    public async Task SendMessage(string user, string message)
        => await Clients.All.SendAsync("ReceiveMessage", user, message);
}

```

## Context Object In Hub

The Hub class includes a Context property that contains the following properties with information about the connection:

**Properties**

* ConnectionId
* User
* UserIdentifier
* Items
* Features
* ConnectionAborted

## Clients object In Hub

**Properties**

* All
* Caller
* Others

## How to send messages to clients ?

**Send to all clients**

``` c#
public async Task SendMessage(string user, string message)
    => await Clients.All.SendAsync("ReceiveMessage", user, message);
```

**Send to Caller**

``` c#
public async Task SendMessageToCaller(string user, string message)
    => await Clients.Caller.SendAsync("ReceiveMessage", user, message);
```

**Send to a Group**

``` c#
public async Task SendMessageToGroup(string user, string message)
    => await Clients.Group("SignalR Users").SendAsync("ReceiveMessage", user, message);
```

## Python Signalrcore client

We were using singalrcore client for communicating with the signalr server.

More about singalcore client module for python : [https://pypi.org/project/signalrcore/]()

## Creating Client

``` python
from signalrcore.hub_connection_builder import HubConnectionBuilder

server_url = "https://localhost:5001/bikesHub"

hub_connection = HubConnectionBuilder()\
    .with_url(server_url, options={"verify_ssl": False})\
    .build()

hub_connection.start()

hub_connection.on_open(lambda: print("connection opened and handshake received ready to send messages"))
hub_connection.on_close(lambda: print("connection closed"))

def on_bikes_info_update(bikesInfo):
    print("Simple Bikes info" + bikesInfo);

hub_connection.on("UpdateBikeName", on_bikes_info_update)

input("Enter to quit >>")

hub_connection.stop()
```

