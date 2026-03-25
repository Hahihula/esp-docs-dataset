

```markdown
Note that the instruction bus shares the same address space (32 MB) with the data bus to access the external memory.

### 4.3.3.2 Cache

As shown in Figure 4.3-2, ESP32-C61 has a shared four-way set-associative cache. Its size is 32 KB and its block size is 32 bytes. The instruction bus and data bus can access the cache simultaneously, but the cache can only respond to one of them at a time through arbitration. If a data missing happens, cache controller initiates a request to the external memory.

![Figure 4.3-2. Cache Structure](image_path)

→: flow of control signals

### 4.3.3.3 Cache Operations

ESP32-C61 cache supports the following operations:

#### 1. Write-back
* Cleans dirty bits in the tag memory and updates new data to external memory.
* After the write-back operation, the new data is updated to external memory.
* This write-back operation does not invalidate the data in the cache, therefore, CPU still can read/write data directly from/to the cache, where data missing will not occur.

#### 2. Write-back & Invalidate
* Cleans dirty bits in the tag memory and updates new data to external memory.
* After the write-back operation, the new data is updated to external memory.
* This operation invalidates the data in the cache, therefore, CPU cannot read/write data directly from/to the cache, where data missing will occur.

#### 3. Clean
* Cleans dirty bits in the tag memory without updating data to external memory.
```