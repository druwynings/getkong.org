---
layout: docs
title: How does it work?
version: 0.1.0beta-3
---

# How does it work?

Kong is made of two different components, that are easy to set up and to scale independently:

* The **Kong Server**, based on a modified version of the widely adopted **NGINX** server, that processes the API requests.
* An underlying **Datastore** for storing operational data, **Apache Cassandra**, which is being used by major companies like Netflix, Comcast or Facebook and it's known for being highly scalable.

Kong needs to have both these components set up and operational. A typical Kong installation can be summed up with the following picture:

![](/assets/images/docs/kong-detailed.png)

Don't worry if you are not experienced with these technologies, Kong works out of the box and you or your engineering team will be able to set it up quickly without issues. Feel free to contact us for any technical question.

## Kong Server

The Kong Server, built on top of **NGINX**, is the server that will actually process the API requests and execute the configured plugins to provide additional functionalities to the underlying APIs before proxying the request to the final destination.

The Proxy Server listens on two ports, that by default are:

* Port `8000`, that will be used to process the API requests.
* Port `8001`, called **admin port**, provides the Kong's internal RESTful API that you can use to operate Kong, and should be private and firewalled.

You can use the **admin port** to configure Kong, create new users, installing or removing plugins, and a handful of other operations. Since you will be using a RESTful API to operate Kong, it is also extremely easy to integrate Kong with existing systems.
