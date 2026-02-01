**Title: Functional Description**

---

### 4.1.2.2 External Memory

ESP32-S2 supports multiple external GSPI/OSPI flash and RAM chips. It also supports hardware encryption/decryption based on XTS-AES to protect developers’ programs and data in flash and RAM.

The external flash and RAM can be mapped into the CPU instruction memory space and read-only data memory space. The RAM can also be mapped into the CPU data memory space. Up to 1 GB of external flash and RAM can be supported.

Through high-speed caches, ESP32-S2 can support the following mappings at the same time:
- Up to **7.5 MB** of instruction memory space can be mapped at a time into flash and RAM. If more than *3.5 MB* are mapped, cache performance may be slightly reduced due to the CPU’s pipeline characteristics.
- Up to **4 MB** of read-only data memory space can be mapped into flash or RAM as individual 64 KB blocks. 8-bit, 16-bit and 32-bit reads are supported.

- Up to **10.5 MB** of read-write data memory space can be mapped into RAM as individual 64 KB blocks.
  - *8-bit*, *16-bit* and *32-bit* reads and writes are supported.* Blocks from this *10.5 MB* space can also be mapped into flash, for read operations only.

**Note:**
After ESP32-S2 is initialized, firmware can customize the mapping of external RAM or flash into the CPU address space.
For more information, please refer to Chapter [ESP32-S2 Technical Reference Manual](#) > Chapter System and Memory.

---

### 4.1.2.3 Cache

ESP32-S2 has independent instruction Cache and data Cache that have the following features:
- Configurable size of *8 KB* or *16 KB*
- **4-way** set associative
- Block size of *16 bytes* or *32 bytes*
- Pre-load function
- Lock function
- Support for critical word first and early restart

---

### 4.1.3 System Components

This subsection describes the essential components that contribute to the overall functionality and control of the system.

---

### 4.1.3.1 Clock

For more information, please refer to [ESP32-S2 Technical Reference Manual](#) > Chapter Reset and Clock.
Espressif Systems
Page: **35**
Document Title: ESP32-S2 Series Datasheet v1.8