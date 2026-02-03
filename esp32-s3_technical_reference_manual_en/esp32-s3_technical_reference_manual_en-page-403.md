**Chapter Title:**
Chapter 4 System and Memory

**Table Title:**
Table 4-3-1. Internal Memory Address Mapping

| Bus Type       | Boundary Address   | High Address    | Size (KB) | Target                   |
|----------------|--------------------|-----------------|-----------|--------------------------|
| Data bus       | Low                |                 |           |                          |
|                | 0x3FF0_0000        | 0x3FF1_FFFF     | 128       | Internal ROM 1          |
|                | 0x3FC8_8000        | 0x3FCE_FFFF     | 416       | Internal SRAM 1         |
|                | 0x3FCF_0000        | 0x3FCF_FFFF     | 64        | Internal SRAM 2         |
|                | 0x4000_0000        | 0x4003_FFFF     | 256       | Internal ROM 0          |
| Instruction bus| Low                |                 |           |                          |
|                | 0x4004_0000        | 0x4005_FFFF     | 128       | Internal ROM 1          |
|                | 0x4037_0000        | 0x4037_FFFF     | 32        | Internal SRAM 0         |
| Data/Instruction bus| Low   |                 |           |                          |
|                    | 0x4037_0000       | 0x403D_FFFF    | 416       | Internal SRAM 1         |
|                    | 0x5000_0000        | 0x5000_1FFF     | 8         | RTC SLOW Memory         |
|                    | 0x600F_E000        | 0x600F_FFFF     | 8         | RTC FAST Memory         |

**Note:**
All of the internal memories are managed by Permission Control module. An internal memory can only be accessed when it is allowed by Permission Control, then the internal memory can be available to the CPU. For more information about Permission Control, please refer to Chapter 15 Permission Control (PMS).

**Subsections and Descriptions:**

1. **Internal ROM 0**
   - Internal ROM 0 is a 256 KB read-only memory space, addressed by the CPU only through the instruction bus as shown in Table 4-3-1.

2. **Internal ROM 1**
   - Internal ROM 1 is a 128 KB read-only memory space, addressed by the CPU through the instruction bus via 0x4004_0000 ~ 0x4005_FFFF or through the data bus via 0x3FF0_0000 ~ 0x3FF1_FFFF in the same order as shown in Table 4-3-1.
   - This means, for example, addresses 0x4004_0000 and 0x3FF0_0000 correspond to the same word; 0x4004_0008 corresponds with a different byte within that address.

3. **Internal SRAM 0**
   - Internal SRAM 0 is a 32 KB read-and-write memory space, addressed by the CPU through the instruction bus as shown in Table 4-3-1.
   - A 16 KB or the total 32 KB of this memory space can be configured as instruction cache (ICache) to store instructions or read-only data from external memory. In this case, occupied memory cannot still access by CPU while remaining parts are accessible.

4. **Internal SRAM 1**
   - Internal SRAM 1 is a 416 KB read-and-write memory space, addressed by the CPU through the data bus or instruction bus in order as shown in Table 4-3-1.
   - The total of these blocks comprises multiple sub-memory (8 KB and 16 KB) with up to 16 KB block used for Trace Memory which can still be accessed.

**Footer:**
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback