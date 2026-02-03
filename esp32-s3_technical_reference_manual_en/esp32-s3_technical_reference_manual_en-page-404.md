**Chapter 4: System and Memory**

---

### GoBack

#### Section Title:
5. Internal SRAM 2

Internal SRAM 2 is a 64 KB, read-write memory space, addressed by the CPU through the data bus, as shown in Table **4.3-1**.

A 32 KB or the total 64 KB can be configured as data cache (DCache) to cache the data of the external memory.
The space used as DCache cannot be accessed by the CPU, while the remaining space can still be accessed
by the CPU.

---

#### Section Title:
6. RTC FAST Memory

RTC FAST Memory is a 8 KB, read-and-write SRAM, addressed by the CPU through the data/instruction bus via 
the shared address **0x600F_E000 ~ 0x600F_FFFF**, as described in Table **4.3-1**.

---

#### Section Title:
7. RTC SLOW Memory

RTC SLOW Memory is a 8 KB read-and-write SRAM, addressed by the CPU through the data/instruction bus via 
shared address **0x5000_E000 ~ 0x5001_FFFF**, as described in Table **4.3-1**.

RTC SLOW Memory can also be used as a peripheral addressable to the CPU via **0x6002_1000 ~ 
0x6002_2FFF**.

---

#### Section Title:
4.3.3 External Memory

ESP32-S3 supports SPI, Dual SPI, Quad SPI, Octal SPI, QPI, and OPI interfaces that allow connection to
external flash and RAM.
It also supports hardware encryption and decryption based on XTS_AES algorithm to protect users’ programs and data in the external flash and RAM.

---

#### Section Title:
4.3.3.1 External Memory Address Mapping

The CPU accesses the external memory via the cache. According to information inside the MMU (Memory 
Management Unit), the cache maps the CPU’s instruction/data bus address into a physical address of the
external flash and RAM.
Due to this address mapping, ESP32-S3 can address up to 1 GB external flash and **1 GB** external RAM.

Using the cache, ESP32-S3 is able to support the following address space mappings at a time:

- Up to **32 MB** instruction bus address space can be mapped to the external flash or RAM as individual 
64 KB blocks via the ICache. 4-byte aligned reads and fetches are supported.
  
- Up to **32 MB** data bus address space can be mapped to the external RAM as individual 64 KB blocks via
the DCache. Single-byte, double-byte, 4-byte, 16-byte aligned reads and writes are supported.

This 
address space can also be mapped to the external flash or RAM for read operations only.
  
Table **4.3-2** lists the mapping between the cache and the corresponding address ranges on the data bus and
instruction bus.


---

#### Table Title:
Table 4.3-2. External Memory Address Mapping

| Bus Type       | Boundary Address   | Size (MB) | Target     |
|----------------|--------------------|-----------|------------|
| Data bus       | **0x3C00_0000**    |            | DCache     |
| Instruction bus| **0x4200_0000**    | 32        | ICache     |

---

Espressif Systems  
ESP32-S3 TRM (Version 1.7)  

[Submit Documentation Feedback](#)