---
title: System Design
tags:
  - System
type: O
DateStarted: 2023-03-13
DateModified: 2024-04-17
status: 
---

# System Design

## Reference

### [System Design for Beginners Course - YouTube](https://www.youtube.com/watch?v=m8Icp_Cid5o)

### [Systems Design Interview Concepts (for software engineers / full-stack web) - YouTube](https://www.youtube.com/watch?v=REB_eGHK_P4)

### [System Design Course for Beginners - YouTube](https://www.youtube.com/watch?v=MbjObHmDbZo)

### 📌[Distributed System Design-分布式技术架构](Distributed-System-Design-分布式技术架构.md)

## Client-Server Model

### DNS query > IP address

- IP address
  - Unique identifier for a machine
  - Like a mailbox some entity has granted to a machine
  - on Unix
    - `dig google.com`
      - will return IP address

### HTTP request to IP address

- able to send information that server understands
- be packed into package
- contain _source address_ of the request
  - the address of the browser
  - for the server to know where it should send a response to
- Ports
  - Server listens for request on specific ports
    - Any machine with a distinct IP address has 16000 ports that programs can listen to
  - need to specify what port you want to communicate on
  - Most clients know the port that they should use depending on the protocol they speak to the server with
    - HTTP
      - Port: 80
    - HTTPS
      - Port: 443
    - Unix tool: netcat
      - `nc -l 8081`
      - `nc 127.0.0.1 8081`
        - A special IP address that always point to your local machine
        - Enter a communication channel
        - Then when typing information on this terminal, the info will appear in the other terminal too
      - allow to read from or write to connections using certain protocols

### Server responds

### Browser receives the server's response and renders HTML on the page

## ⭐[Network Protocols-网络协议](Network-Protocols-网络协议)

### IP

### TCP

### HTTP

## Storage

## Latency and Throughput

## Availability

## [Caching](Caching.md)

## Proxies

## [Load Balancing](Load-Balancing.md)

## Hashing

## [Database](Database.md)

### [Database Scaling and Design](Database-Scaling-and-Design.md)

### [SQL DB](SQL-DB.md)

### Key-Value Stores

### Specialized Storage Paradigms

### Replication and Sharding

## Leader Election

## Peer-to-peer networks

## Polling and Streaming

## Configuration

## Rate Limiting

## Logging and Monitoring

## Publish-Subscribe Pattern

## MapReduce

## Security and HTTPs

## [API Design](API-Design.md)

## [Design a YouTube Clone](Design-a-YouTube-Clone.md)
