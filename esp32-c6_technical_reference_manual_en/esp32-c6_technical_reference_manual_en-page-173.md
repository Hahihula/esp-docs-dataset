

```markdown
Chapter 5 System and Memory

GoBack

5.3.3.2 Cache

As shown in Figure 5.3-1, ESP32-C6 has a read-only uniform cache which is four-way set-associative. Its size is 32 KB and its block size is 32 bytes. The cache is accessible by the instruction bus and the data bus at the same time, but can only respond to one of them at a time. When a cache miss occurs, the cache controller will initiate a request to the external memory.

![Figure 5.3-1. Cache Structure](image)

Figure 5.3-1. Cache Structure

5.3.3.3 Cache Operations

ESP32-C6 cache supports the following operations:

1. Invalidate: This operation is used to remove valid data in the cache. Once this operation is done, the deleted data is stored only in the external memory. If the HP CPU wants to access the data again, it needs to access the external memory. There are two types of invalidate operation: Invalidate-All and Manual-Invalidate. Manual-Invalidate is performed only on data in the specified area in the cache, while Invalidate-All is performed on all data in the cache.

2. Preload: This operation is to load instructions and data into the cache in advance. The minimum unit of preload-operation is one block. There are two types of preload-operation: manual preload (Manual-Preload) and automatic preload (Auto-Preload). Manual-Preload means that the hardware prefetches a piece of continuous data according to the virtual address specified by the software. Auto-Preload means the hardware prefetches a piece of continuous data according to the current address where the cache hits or misses (depending on configuration).

3. Lock/Unlock: The lock operation is used to prevent the data in the cache from being easily replaced. There are two types of lock: prelock and manual lock. When prelock is enabled, the cache locks the data in the specified area when filling the missing data to cache memory, while the data outside the specified area will not be locked. When manual lock is enabled, the cache checks the data that is already in the cache memory and locks the data only if it falls in the specified area, and leaves the data outside the specified area unlocked. When there are missing data, the cache will replace the data in the unlocked way first, so the data in the locked way is always stored in the cache and will not be replaced. But when all ways within the cache are locked, the cache will replace data, as if it was not locked. Unlocking is the reverse of locking, except that it only can be done manually.
```