

```markdown
Manual-Invalidate. Manual-invalidiate is performed only on data in the specified area in the cache, while Invalidate-All is performed on all data in the cache.

2. Preload: This operation is to load instructions and data into the cache in advance. The minimum unit of preload-operation is one block. There are two types of preload-operation: manual preload (Manual-Preload) and automatic preload (Auto-Preload). Manual-Preload means that the hardware prefetches a piece of continuous data according to the virtual address specified by the software. Auto-Preload means the hardware prefetches a piece of continuous data according to the current address where the cache hits or misses (depending on configuration).

3. Lock/Unlock: The lock operation is used to prevent the data in the cache from being easily replaced. There are two types of lock: prelock and manual lock. When prelock is enabled, the cache locks the data in the specified area when filling the missing data to cache memory, while the data outside the specified area will not be locked. When manual lock is enabled, the cache checks the data that is already in the cache memory and locks the data only if it falls in the specified area, and leaves the data outside the specified area unlocked. When there are missing data, the cache will replace the data in the unlocked way first, so the data in the locked way is always stored in the cache and will not be replaced. But when all ways within the cache are locked, the cache will replace data, as if it was not locked. Unlocking is the reverse of locking, except that it only can be done manually.

Please note that Manual-Invalidate operation only works on the unlocked data. If you expect to perform such operation on the locked data, please unlock them first.
```

## 4.3.4 GDMA Address Space

The General Direct Memory Access (GDMA) peripheral consisting of three TX channels and three RX channels provides Direct Memory Access (DMA) service, including:

*   data transfers between different locations of internal memory
*   data transfers between modules/peripherals and internal memory

GDMA uses the same addresses as the data bus to access HP SRAM, i.e., GDMA uses address range `0x4080_0000 ~ 0x4084_FFFF` to access HP SRAM.

Eight modules/peripherals in ESP32-H2 work together with GDMA. As shown in Figure 4.3-2, eight vertical lines correspond to these eight modules/peripherals with GDMA function. The horizontal line represents a certain channel of GDMA (can be any channel), and the intersection of the vertical line and the horizontal line indicates that a module/peripheral has the ability to access the corresponding channel of GDMA. If there are multiple intersections on the same line, it means that these peripherals/modules can not enable the GDMA function at the same time.
```