___
A cache is a hardware or software component that ==stores data== so that future requests for data can be served **faster**. The data stored in a cache might be a result of an earlier computation or a copy of data stored elsewhere. It improves system performance by reducing access to slower storage layers like main memory, disks, or remote servers. Caching is widely used in CPU architecture, operating systems, databases, web browsers, and distributed systems.
___
###### Keywords
- **Cache**
    - A small, fast storage area that holds copies of frequently accessed data.
- **Cache Hit**
    - When requested data is found in the cache.
- **Cache Miss**
    - When requested data is not found in the cache and must be fetched from slower storage.
- **Latency**
    - The time taken to retrieve data.
- **Throughput**
    - The amount of data processed per unit time.
- **Temporal Locality**
    - Recently accessed data is likely to be accessed again soon.
- **Spatial Locality**
    - Data near recently accessed memory locations is likely to be accessed.
- **Eviction Policy**
    - Rules that determine which data is removed from the cache when it is full.
- **TTL (Time To Live)**
    - The duration data remains valid in the cache.
- **Cache Invalidation**
    - The process of removing or updating stale data in the cache.
___
###### How Caching Works
When a system requests data, it first checks the cache:
- If the data is found, this is called a **cache hit**, and the data is returned immediately.
- If the data is not found, this is a **cache miss**, and the system must retrieve the data from slower storage before optionally storing it in the cache for future use.

Well-designed caching systems aim to ==maximize cache hits== and ==minimize cache misses==. **Temporal locality** means that data accessed recently is likely to be accessed again soon. **Spatial locality** means that data stored near recently accessed data is also likely to be accessed. These principles explain why caches are effective even when they are much smaller than the total data.
___
###### Types of Cache
1. **CPU Cache**
    - Located on the processor (L1, L2, L3).
    - Extremely fast but very small.
2. **Memory Cache**
    - Uses RAM to store frequently used data.
    - Example: application-level caching.
3. **Web / HTTP Cache**
    - Caches HTTP responses (e.g., browsers, CDNs).
    - Reduces repeated server requests.
4. **Distributed Cache**
    - Shared cache across multiple machines.
    - Examples: [[Redis]].
---
###### Cache Eviction Policies
Because cache space is limited, old date must be removed to make room for new entries this process is called cache eviction. 

Some common strategies are: 
- **LRU (Least Recently Used)**
    - Removes the data that hasn’t been accessed recently.
    - Involves associating a TTL with data.
- **LFU (Least Frequently Used)**
    - Removes the least accessed data.
- **FIFO (First In, First Out)**
    - Removes the oldest cached entry.
- **Random**
    - Removes a random entry.
---
###### Cache Write Strategies
1. **Write-Through**
    - Data is written to cache and main storage simultaneously.
2. **Write-Back (Write-Behind)**
    - Data is written to cache first, then to storage later.
3. **Write-Around**
    - Data is written directly to storage, bypassing cache.
---
![[top-caching-strategies.png]]
___
## Common Use Cases
- Speeding up database queries
- Reducing API response time
- Lowering server and network load
- Improving application scalability and user experience
---
## Flashcards
#flashcards
**What is cache in computing?** :: A cache is a hardware or software component that stores data so that future requests for data can be served **faster**.

**What is a cache hit?** :: When requested data is found in the cache.

**What is a cache miss?** :: When requested data is not found in the cache and must be fetched from slower storage.

**Why does caching improve performance?** :: It reduces access time to slow storage layers.

**What is temporal locality?** :: Recently accessed data is likely to be accessed again soon.

**What is spatial locality?** :: Data near recently accessed memory locations is likely to be accessed.

**What is cache eviction?** :: The removal of data from cache when space is needed.

**What does LRU stand for?** :: Least Recently Used.

**What is TTL in caching?** :: Time To Live how long cached data remains valid.

**What is cache invalidation?** :: The process of removing or updating stale cached data.

**What is a distributed cache?** :: A cache shared across multiple systems or servers.

**Give an examples of a distributed cache system.** :: Redis

**What is write-through caching?** :: Data is written to cache and storage at the same time.

**What is write-back caching?** :: Data is written to cache first and storage later.

**Why is cache important in web applications?** :: It improves response times, reduces load, and increases scalability.