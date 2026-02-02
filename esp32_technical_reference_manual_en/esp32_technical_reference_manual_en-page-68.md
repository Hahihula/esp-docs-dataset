**Chapter Title:**
Chapter 3 System and Memory

**Table Title:**
Table 3.3-2. Embedded Memory Address Mapping

| Bus Type | Boundary Address Low Address       | High Address   | Size    | Target     | Comment               |
|----------|-------------------------------------|-----------------|---------|------------|-----------------------|
|          |                                     |                 |         |            |                       |
| Data     | 0x3FF8_0000                         | 0x3FF8_1FFF     | 8 KB    | RTC FAST Memory | PRO_CPU Only          |
| Data     | 0x3FF8_2000                         | 0x3FF8_FFFF     | 56 KB   | Reserved   | -                     |
| Data     | 0x3FF9_0000                         | 0x3FF9_FFFF     | 64 KB   | Internal ROM1 | -                     |
| Data     | 0x3FAA_DFFF                          | 0x3FAA_FFFF     | 56 KB   | Reserved   | -                     |
| Data     | 0x3FFA_E000                         | 0x3FFD_FFFF     | 200 KB  | Internal SRAM2| DMA                   |
| Data     | 0x3FFE_0000                         | 0x3FFE_FFFF     | 128 KB  | Internal SRAM1| DMA                   |

**Subsections:**

- **3.3.2.1 Internal ROM 0**
  - The capacity of Internal ROM 0 is 384 KB. It is accessible by both CPUs through the address range 0x4000_0000 ~ 0x4005_FFFF, which is on the instruction bus.
  - The address range of the first 32 KB of the ROM O (0x4000_0000 ~ 0x4007FFF) can be remapped in order to access a part of Internal SRAM1 that normally resides in a memory range of 0x400B_0000 ~ 0x400B_7FFF.
  - While remapping, the 32 KB SRAM cannot be accessed by an address range of 0x400B_0000 ~ 0x400B_7FFF anymore but it can still be accessible through the data bus (0x3FE8_8000 ~ 0x3FFE_FFFF).
  - This can be done on a per-CPU basis: setting bit O of register DPOR_PROBOOT_REMAP_CTRL_REG or DPORT_APP_BOOT_REMAP_CTRL_REG will remap SRAM for the PRO_CPU and APP_CPU, respectively.

- **3.3.2.2 Internal ROM 1**
  - The capacity of Internal ROM 1 is 64 KB. It can be read by either CPU at an address range 0x3FF9_0000 ~ 0x3FF9_FFFF of the data bus.

- **3.3.2.3 Internal SRAM O**
  - The capacity of Internal SRAM O is 192 KB. Hardware can be configured to use the first 64 KB to cache external memory access.
  - When not used as cache, the first 64 KB can be read and written by either CPU at addresses.

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:** 
68