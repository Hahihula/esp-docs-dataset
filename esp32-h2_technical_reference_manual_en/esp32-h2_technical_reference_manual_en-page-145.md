

```markdown
Chapter 4 System and Memory

GoBack

This 4 KB LP SRAM is a read-and-write memory, accessed by the CPU through the instruction bus or through the data bus via their shared address 0x5000_0000 ~ 0x5000_OFFF as shown in Table 4.3-1.

4.3.3 External Memory

ESP32-H2 supports SPI, Dual SPI, Quad SPI, and QPI interfaces that allow connection to external flash. ESP32-H2 also supports hardware manual encryption and automatic decryption based on XTS-AES algorithm to protect users' programs and data in the external flash.

4.3.3.1 External Memory Address Mapping

The CPU accesses the external memory via the cache. According to information inside the MMU (Memory Management Unit), the cache maps the CPU's address (0x4200_0000 ~ 0x42FF_FFFF) into a physical address of the external memory. Due to this address mapping, ESP32-H2 can address up to 16 MB external flash. Note that the instruction bus shares the same address space (16 MB) with the data bus to access the external memory.

4.3.3.2 Cache

As shown in Figure 4.3-1, ESP32-H2 has a read-only uniform cache which is eight-way set-associative. Its size is 16 KB and its block size is 32 bytes.

The instruction bus and data bus can access the Cache simultaneously, but the Cache can only respond to one of them at a time through arbitration. When a cache miss occurs, the cache controller will initiate a request to the external memory.

![Figure 4.3-1. Cache Structure](#)

CPU
instruction bus
data bus (read-only)
Cache
MMU
External Memory

Figure 4.3-1. Cache Structure

4.3.3.3 Cache Operations

ESP32-H2 cache supports the following operations:

1. Invalidate: This operation is used to remove valid data in the cache. Once this operation is done, the deleted data is stored only in the external memory. If the CPU wants to access the data again, it needs to access the external memory. There are two types of invalidate operation: Invalidate-All and
```