## Caching

### What?

When you cache something, you take data that would normally be stored on a hard drive or a disk, you put it into memory.

### Why?

- Improve speed and performance of your application
  - Reading from memory is 50-200x faster than disk
  - Can serve the same amount of traffic with fewer resources
  - Pre-calculate and cache data
  - Most apps have more reads than writes, perfect for caching
- Save money  
  ![](z-Assets/Pasted%20image%2020230315171153.png)

### Caching Layers

![](z-Assets/Pasted%20image%2020230315172151.png)

#### DNS

- Go to DNS once to get the IP and store it on the client

#### CDN

- Content Distribution Network, eg. Cloudflare
- Store static files like pictures and videos

#### Application

#### Database

- Cache sits in front of DB to handle serving content
- Can't cache everything (Dynamic data)
- Tools
  - Redis
  - Memcached

#### Distributed Cache

- Has built-in functionality to replicate data , shared data across servers, and locate proper server for each key
- Replication
- ![](z-Assets/Pasted%20image%2020230315172830.png)

### Cache Eviction

##### Why?

- Prevent stale data
- Caching only tmost valuable data to save resources

##### How

- TTL-Time to live
  - Set a time period before a cache entry is deleted
  - To prevent stale data
- LRU- Least recently used
  - Once cache is full, remove last accessed key and add new key
- LFU-Least frequently used
  - Track number of times key is accessed
  - Drop least used when cache is full

### Caching Strategies

### Cache Consistency
