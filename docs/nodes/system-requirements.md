---
tags: [Nodes]
description: Avalanche is an incredibly lightweight protocol, so nodes can run on commodity hardware. Note that as network usage increases, hardware requirements may change.
sidebar_label: System Requirements
pagination_label: System Requirements for Running an Avalanche Node
---

# System Requirements for Running an Avalanche Node

## Hardware and Operating Systems

Avalanche is an incredibly lightweight protocol, so nodes can run on commodity
hardware. Note that as network usage increases, hardware requirements may
change.

- CPU: Equivalent of 8 AWS vCPU
- RAM: 16 GiB
- Storage: 1 TiB SSD
- OS: Ubuntu 20.04 or MacOS &gt;= 12

:::caution

Please do not try running a node on an HDD, as you may get poor and random 
read/write latencies, therefore reducing performance and reliability.

:::

## Networking

To run successfully, AvalancheGo needs to accept connections from the Internet
on the network port `9651`. Before you proceed with the installation, you need
to determine the networking environment your node will run in.

### Running on a Cloud Provider

If your node is running on a cloud provider computer instance, it will have a
static IP. Find out what that static IP is, or set it up if you didn't already.

### Running on a Home Connection

If you're running a node on a computer that is on a residential internet
connection, you have a dynamic IP; that is, your IP will change periodically.
You will need to set up inbound port forwarding of port `9651` from the internet
to the computer the node is installed on.

As there are too many models and router configurations, we cannot provide
instructions on what exactly to do, but there are online guides to be found
(like
[this](https://www.noip.com/support/knowledgebase/general-port-forwarding-guide/),
or [this](https://www.howtogeek.com/66214/how-to-forward-ports-on-your-router/)
), and your service provider support might help too.

:::warning

A fully connected Avalanche node maintains and communicates
over a couple of thousand of live TCP connections. For some low-powered and
older home routers that might be too much to handle. If that is the case you may
experience lagging on other computers connected to the same router, node getting
benched, failing to sync and similar issues.

:::
