**Chapter Title:**
Chapter 3 System and Memory

**GoBack Button**

---

**Section Heading:**
3.3 Functional Description

**Subsection Heading:**
3.3.1 Address Mapping

**Body Text:**
Each of the two Harvard Architecture Xtensa LX6 CPUs has 4 GB (32-bit) address space. Address spaces are symmetric between the two CPUs.

Addresses below 0x4000_0000 are serviced using the data bus. Addresses in the range 0x4000_0000 ~ 0x4FFF_FFFF are serviced using the instruction bus. Finally, addresses over and including 0x5000_0000 are shared by the data and instruction bus.

The data bus and instruction bus are both little-endian: for example, byte addresses 0x0, 0x1, 0x2, 0x3 access the least significant, second least significant, second most significant, and the most significant bytes of the 32-bit word stored at the 0x0 address, respectively. The CPU can access data bus addresses via aligned or non-aligned byte, half-word and word read-and-write operations. The CPU can read and write data through the instruction bus, but only in a **word aligned manner**: non-word-aligned access will cause a CPU exception.

Each CPU can directly access embedded memory through both the data bus and the instruction bus, external memory which is mapped into the address space (via transparent caching & MMU), and peripherals. Table 3.3-1 illustrates address ranges that can be accessed by each CPU’s data bus and instruction bus.

Some embedded memories and some external memories can be accessed via the data bus or the instruction bus. In these cases, the same memory is available to either of the CPUs at two address ranges.

**Table Title:**
Table 3.3-1. Address Mapping

| Bus Type | Low Address       | Boundary Address | High Address      | Size         | Target    |
|----------|-------------------|------------------|--------------------|--------------|-----------|
| Data     | 0x0000_0000      |                   | 0x3F3F_FFFF        | Reserved     |           |
|          | 0x3F40_0000      |                   | 0x3F7F_FFFF        | 4 MB         | External Memory |
|          | 0x3F80_0000      |                   | 0x3FBF_FFFF        | 4 MB         | External Memory |
|          | 0x3FC0_0000      |                   | 0x3FEF_FFFF        | Reserved     |           |
| Data     | 0x3FF0_0000      |                   | 0x3FF7_FFFF        | 512 KB       | Peripheral |
|          | 0x3FF8_0000      |                   | 0x3FFF_FFFF        | 512 KB       | Embedded Memory |
| Instruction | 0x4000_0000   |                   | 0x400C_1FFF        | 776 KB       | Embedded Memory |
|           | 0x400C_2000     |                   | 0x40BF_FFFF        | 11512 KB     | External Memory |
|           | 0x40C0_0000     |                   | 0x4FFF_FFFF        | 244 MB       | Reserved   |
| Data / Instruction | 0x5000_0000    |                   | 0x5000_1FFF        | 8 KB         | Embedded Memory |
|          | 0x5000_2000     |                   | 0xFFFF_FFFF        | Reserved     |           |

**Subsection Heading:**
3.3.2 Embedded Memory

**Body Text:**
The Embedded Memory consists of four segments: internal ROM (448 KB), internal SRAM (520 KB), RTC FAST memory (8 KB) and RTC SLOW memory (8 KB).

**Footer Information:**
Espressif Systems
66 ESP32 TRM (Version 5.6)
Submit Documentation Feedback