---
Title: Protocols-网络协议
Type: O
tags:
  - Network
DateDo: 
DateDone: 
DateStarted: 2023-03-06
DateModified: 2023-12-27
DateDue: 
status: 
mindmap-plugin: basic
---

# Network Protocols

## Reference

### [Protocol - MDN Web Docs Glossary: Definitions of Web-related terms | MDN](https://developer.mozilla.org/en-US/docs/Glossary/Protocol)

### [[Web, Network, Internet]]

### [[S-Network]]

## Intro

### Protocol
- Rules for interactions between two parties

### Network protocol
- the type of messages that are going to be sent over the network
- format, structure  and order of those messages
- whether or not there should be some sort of response, and what the response should look like
- whether or not there should be rules around when messages can be sent to one another

## [[TCP-IP]]

### Network layers and TCP/IP

### IP
- Internet Protocol
- IP address
- Versions
    - IPv4
    - IPv6
- Data is to be sent in the form of an *IP packet*
    - The building blocks of communication between machines over the Internet
    - The fundamental unit of data made up of *Bytes*
        - There are other units beyond IP packets
    - 2 sections
        - Header
            - Source address of the packet
            - Destination address the packet is going to
            - Total size of the packet
            - Version of the Internet protocol that this IP packet is operating by
            - Size of the header
                - Small: 20~60 Bytes
        - Data
            - Size limit
                - 0~65 mb
                - ❌Data lost, and wrong order for multiple IP packets
            - TCP header

### TCP
- Transmission control protocol
    - ✅To send IP packet in an ordered way
- To communicate with another machine
    - Create a TCP connection with the destination server through a *handshake*, a special TCP interaction where one computer contacts the other by sending a packet or a few packets
    - The server responds saying OK
    - The client re-responds saying OK
    - Then, both machines can freely sends data to one another
    - Cases
        - Timeout
            - If one of the machines doesn't send data in a given amount of time
        - End connection by sending special message
- ❌You're just sending arbitrary data that fits into these underlying IP packets

## [[HTTP]]

### Introduce a higher level abstraction above TCP and IP
- *Request-Response Paradigm*

### With HTTP, all we deal with are HTTP request and response

### Request
- have lots of *properties* defined by HTTP protocol
- host
- port
- method
    - post
        - provide data to the server
    - get
        - retrieve data from the server
    - put
    - delete
        - ask the server to delete data
- path
    - A server might have multiple paths for different services
    - Separate out logic on the server
- headers
    - `'content-type': 'application/json'`
        - Type of the body
    - `'content-length':51`
- body

### Response
- *statusCode*
    - Type of response

### Express server example
- ![[z-express-server-example.png]]
- Accept json as the data format
- Listen to port 3000
- 2 endpoints
- Unix
    - Launch server
        - `node server.js`
    - `curl`
        - Allow to send data to servers and retrieve data from servers using different protocols
        - Default: get request
            - `curl localhost:3000/hello`
        - Default: post request
            - `curl --header 'content-type: application/json' localhost:3000/hello --data'{"foo":"bar"}'`

## [[HTTP]]/ [[HTTPS-HTTPS2]]/ [[DNS]]

## IP/ ICMP

## TCP/ UDP

## ARP/ RARP