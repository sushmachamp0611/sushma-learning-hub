Caching - local store for faster access 
Challenges- Hardware is expensive, cache is volatile (crash restart)

Types
1. Appication cache - within application
2. Distributes cache- each node wil have part of cache and using it with consistent hashing mechnanism
3. Global cache - edge sever CDN

Applications/Benefits: reduce load, and increased speed
Web page caching, DB caching, CDN, session caching, API response caching 

Cache invalidation strategies 
- time based
- Event based

Eviction policy decides which existing item to evict  which cache is full
- LRU - Popular strategy - Last recently used 
- LFU - Least frequestly used
- FIFO evicting the oldest cached

  Cons: Data inconsistency, additional complexity, cost of cache, cache eviction issues 

Strategies: 
1. Read through : appln reads only from cache : ORM framework: single API
2. Write through: Writes to cache and DB simultaneously 
3. Write behind: updates cache first and asynchronously updates DB
4. Cache aside: Access cache , if cache miss then only accesses DB
