Caching - local store for faster access 
Challenges- Hardware is expensive, cache is volatile (crash restart)

Types
1. Appication cache - within application
2. Distributes cache- each node wil have part of cache and using it with consistent hashing mechnanism
3. Global cache - edge sever SDN

Applications: reduce load, and increased speed
Web page caching, DB caching, CDN, session caching, API response caching 

Cache invalidation strategies 
- time based
- Event based

Eviction policy decides which existing item to evict  which cache is full
- LRU - Popular strategy - Last recently used 
- LFU - Least frequestly used
- FIFO evicting the oldest cached

  Cons: Data inconsistency, additional complexity, cost of cache, cache eviction issues 
