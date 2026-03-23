

```markdown
## 3.3.3.1 External Memory Address Mapping

The CPU accesses the external memory via the cache. According to the MMU (Memory Management Unit) settings, the cache maps the CPU’s address to the external memory’s physical address. Due to this address mapping, the ESP32-C3 can address up to 16 MB external flash.

Using the cache, ESP32-C3 is able to support the following address space mappings. Note that the instruction bus address space (8MB) and the data bus address space (8 MB) is always shared.

* Up to 8 MB instruction bus address space can be mapped into the external flash. The mapped address space is organized as individual 64-KB blocks.
* Up to 8 MB data bus (read-only) address space can be mapped into the external flash. The mapped address space is organized as individual 64-KB blocks.

Table 3.3-2 lists the mapping between the cache and the corresponding address ranges on the data bus and instruction bus.

Table 3.3-2. External Memory Address Mapping

| Bus Type | Boundary Address Low Address | High Address | Size (MB) | Target |
|----------|------------------------------|--------------|-----------|--------|
| Data bus (read-only) | 0x3C00_0000 | 0x3C7F_FFFF | 8 | Uniform Cache |
| Instruction bus | 0x4200_0000 | 0x427F_FFFF | 8 | Uniform Cache |

Note:
Only if the CPU obtains permission for accessing the external memory, can it be responded for memory access.
For more detailed information about permission control, please refer to Chapter 14 Permission Control (PMS).

## 3.3.3.2 Cache

As shown in Figure 3.3-1, ESP32-C3 has a read-only uniform cache which is eight-way set-associative, its size is 16 KB and its block size is 32 bytes. When cache is active, some internal memory space will be occupied by cache (see Internal SRAM 0 in Section 3.3.2).

The uniform cache is accessible by the instruction bus and the data bus at the same time, but can only respond to one of them at a time. When a cache miss occurs, the cache controller will initiate a request to the external memory.
```