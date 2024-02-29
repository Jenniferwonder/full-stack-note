L4 VS L7

##### 3.1. Layer 4

- Only has access to TCP and UDP data
- Faster
- Lack of info can lead to uneven traffic
- Good on the edge of your data center or of your network, because it can look at the IP address and if you're getting a denial of service attack or some bad actors going after application, instead of wasting processing power allowing it through to your web server or your application, you can toss that request at the edge, so lots of data centers will first route all incoming traffic through a layer 4 LB(Load balancer)

##### 3.2. Lyer 7

- Full access to HTTP protocol and data
- SSL termination
- Check for authentication
  - If a user sends a request they're not logged in, they're trying to get to a certain page, instead of letting that go to your application server, at the LB you could redirect those people
- Smarter routing options
  - as a result of having access to the entire url of the request and all the data within that, you have a lot of smarter routing options.
- It's more CPU intensive