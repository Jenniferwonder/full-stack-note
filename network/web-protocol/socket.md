---
title: Socket
topic: 
type: 
tags:
  - Network
DateStarted: 2024-04-11
DateModified: 2024-04-17
Datereviewed: 
reviewed: 
difficulty: 
status: 
comment: 
aliases:
  - Socket
linter-yaml-title-alias: Socket
---

# Socket

#### 套接字（socket）概念

套接字（socket）是通信的基石，是支持 TCP/IP 协议的网络通信的基本操作单元。它是网络通信过程中端点的抽象表示，包含进行网络通信必须的五种信息：

- 连接使用的协议
- 本地主机的 IP 地址
- 本地进程的协议端口
- 远地主机的 IP 地址
- 远地进程的协议端口。  
  应用层通过传输层进行数据通信时，TCP 会遇到同时为多个应用程序进程提供并发服务的问题。**多个 TCP 连接或多个应用程序进程可能需要通过同一个 TCP 协议端口传输数据**。为了区别不同的应用程序进程和连接，许多计算机操作系统为应用程序与 TCP／IP 协议交互提供了套接字 (Socket) 接口。应用层可以和传输层通过 Socket 接口，区分来自不同应用程序进程或网络连接的通信，实现数据传输的并发服务。

#### 建立 Socket 连接

建立 Socket 连接至少需要一对套接字，

- 其中一个运行于客户端，称为 ClientSocket ，
- 另一个运行于服务器端，称为 ServerSocket 。  
  套接字之间的连接过程分为三个步骤：
- 服务器监听，
- 客户端请求，
- 连接确认。  
  服务器监听：服务器端套接字并不定位具体的客户端套接字，而是处于等待连接的状态，实时监控网络状态，等待客户端的连接请求。  
  客户端请求：指客户端的套接字提出连接请求，要连接的目标是服务器端的套接字。为此，客户端的套接字必须首先描述它要连接的服务器的套接字，指出服务器端套接字的地址和端口号，然后就向服务器端套接字提出连接请求。  
  连接确认：当服务器端套接字监听到或者说接收到客户端套接字的连接请求时，就响应客户端套接字的请求，建立一个新的线程，把服务器端套接字的描述发给客户端，一旦客户端确认了此描述，双方就正式建立连接。而服务器端套接字继续处于监听状态，继续接收其他客户端套接字的连接请求。

#### Socket 连接与 TCP 连接

创建 Socket 连接时，可以指定使用的传输层协议，Socket 可以支持不同的传输层协议（TCP 或 UDP），当使用 TCP 协议进行连接时，该 Socket 连接就是一个 TCP 连接。

#### Socket 连接与 HTTP 连接

由于通常情况下 Socket 连接就是 TCP 连接，因此 Socket 连接一旦建立，通信双方即可开始相互发送数据内容，直到双方连接断开。但在实际网络应用中，客户端到服务器之间的通信往往需要穿越多个中间节点，例如 **路由器、网关、防火墙** 等，大部分防火墙默认会关闭长时间处于非活跃状态的连接而导致 Socket 连接断连，因此需要通过轮询告诉网络，该连接处于活跃状态。  
而 HTTP 连接使用的是“请求—响应”的方式，不仅在请求时需要先建立连接，而且需要客户端向服务器发出请求后，服务器端才能回复数据。  
很多情况下，需要服务器端主动向客户端推送数据，保持客户端与服务器数据的实时与同步。此时 **若双方建立的是 Socket 连接，服务器就可以直接将数据传送给客户端**；  
若双方建立的是 HTTP 连接，则服务器需要等到客户端发送一次请求后才能将数据传回给客户端，因此，**客户端定时向服务器端发送连接请求**， 不仅可以保持在线，同时也是在“询问”服务器是否有新的数据，如果有就将数据传给客户端。
