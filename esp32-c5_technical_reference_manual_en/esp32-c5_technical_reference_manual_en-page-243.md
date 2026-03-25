

```markdown
- Users can choose whether to invalidate the data in the cache.
- If the data is not invalidated, HP CPU will read/write data directly from/to the cache where data missing will not occur.

2. Clean

- Clears dirty bits in the tag memory without updating data to external memory.
- After the clean operation, old data remains in external memory, while the cache holds the new one (unaware of it).
- HP CPU can then read/write the data directly from/to the cache, where data missing will not occur.

3. Invalidate

- Clean the valid bits in tag memory. This is to remove valid data from the cache.
- Once this operation is done, the deleted data is stored only in external memory.
- HP CPU needs to access external memory if it wants to access the data again.
- Two types of invalidate operation:
  - Manual-Invalidate: is performed only on data in the specified cache area.
  - Invalidate-All: is performed on all data in the cache.

4. Preload

- Loads instructions and data into the cache in advance.
- Minimum unit of preload operation is one block.
- Two types of preload operation:
  - Manual-Preload: involves the hardware prefetching continuous data based on the virtual address specified by the software.
  - Auto-Preload: involves the hardware prefetching continuous data based on the current address where the cache hits or misses (configuration-dependent).

5. Lock/Unlock

- Lock operation prevents easily replacing data in the cache.
- Two types of lock:
  - Prelock: locks data in the specified area when filling missing data to cache memory, leaving the data outside the specified area unlocked.
  - Manual Lock: checks data in the cache memory and locks data only if it falls in the specified area, leaving data outside the specified area unlocked.
- When there is missing data, the cache replaces the data in the unlocked way first, ensuring that the data in the locked way remains in the cache and will not be replaced.
- When all ways within the cache are locked, the cache will replace data, as if it was not locked.
- Unlocking is the reverse of locking and can only be done manually.
```