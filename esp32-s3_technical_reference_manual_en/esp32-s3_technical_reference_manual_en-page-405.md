**Chapter Title:**
Chapter 4 System and Memory

**Note Section:**
- Only if the CPU obtains permission for accessing the external memory, can it be responded for memory access.
- For more detailed information about permission control, please refer to Chapter 15 Permission Control (PMS).

**Subtitle: 4.3.3.2 Cache**

**Body Text:**
As shown in Figure 4.3-1, ESP32-S3 has a dual-core-shared ICache and DCache structure, which allows prompt response upon simultaneous requests from the instruction bus and data bus. Some internal memory space can be used as cache (see Internal SRAM O and Internal SRAM 2 in Section 4.3.2).

When the instruction bus of two cores initiate a request on ICache simultaneously, the arbiter determines which core gets the access to the ICache first; when the data bus of two cores initiate a request on DCache simultaneously, the arbiter determines which gets the access to the DCache first. When a cache miss occurs, the cache controller will initiate a request to the external memory. When ICache and DCache initiate requests on the external memory simultaneously, the arbiter determines which gets the access to the external memory first. The size of ICache can be configured to 16 KB or 32 KB, while its block size can be configured to 16 B or 32 B. When an ICache is configured to 32 KB, its block cannot be 16 B. The size of DCache can be configured to 32 KB or 64 KB, while its block size can be configured to 16 B, 32 B or 64 B. When a DCache is configured to 64 KB, its block cannot be 16 B.

**Figure Caption:**
Figure 4.3-1. Cache Structure

**Diagram Description (Cache Structure):**
The diagram shows the interaction between CPU Core0 and CPU Core1 with their respective ICache and DCache units connected through an MMU to external memory via instruction bus, data buses, arbiter for cache control.

**Subtitle: 4.3.3.3 Cache Operations**

**Body Text:**
ESP32-S3 caches support the following operations:

1. **Write-Back:** This operation is used to clear the dirty bits in dirty blocks and update the new data to the external memory. After the write-back operation finished, both the external memory and the cache are bearing the new data. The CPU can then read/write the data directly from the cache. Only DCache has this function.

   If the data in the cache is newer than the one stored in the external memory, then the new data will be considered as a dirty block. The cache tracks these dirty blocks through their dirty bits. When the dirty bits of a data are cleared, the cache will consider the data as new.

**Footer:**
Espressif Systems  
405  
ESP32-S3 TRM (Version 1.7)  

**Link Texts:**
- Submit Documentation Feedback
- GoBack