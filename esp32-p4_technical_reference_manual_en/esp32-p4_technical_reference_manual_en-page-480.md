

```markdown
- 64 KB of data cache (dcache) with a 64 B block size, two-way set associative, supporting two writing strategies: write-through and write-back
• L2 cache: 128 KB/256 KB/512 KB with 64 B/128 B block sizes, eight-way set associative
• Cache-able and noncache-able access, depending on CPU PMA
• Preload operation
• Lock operation
• Critical word first and early restart

Figure 7.3-3. Cache Structure

7.3.3.3 Cache Operations

ESP32-P4 I1 cache and I2 cache supports the following operations:

1. Write-back (for dcache and I2 cache only):
    • Clears dirty bits in the tag memory and updates new data to external memory.
    • After the write-back operation, the new data is updated to external memory.
    • Users can choose whether to invalidate the data in the cache.
    • If the data is not invalidated, CPU will read/write data directly from/to the cache where data missing will not occur.

2. Clean (for dcache and I2 cache only):
    • Clears dirty bits in the tag memory without updating data to external memory.
    • After the clean operation, old data remains in external memory, while the cache holds the new one (unaware of it).
```