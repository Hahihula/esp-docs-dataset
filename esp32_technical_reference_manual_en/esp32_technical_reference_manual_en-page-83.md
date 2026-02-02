**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Table of Registers Information:**

| Size | Boundary address Low | High | Register Authority Bit |
|------|-----------------------|-----|-------------------------|
|      |                       |     |                        |
| 8 KB | 0x3FFF_C000           | 0x3FFF_DFFF | DPORT_AHB MPU_TABLE_1_REG   | 7 |
| 8 KB | 0x3FFF_E000           | 0x3FFF_FFFF | DPORT_AHB MPU_TABLE_1_REG   | 8 |

**Text:**

Registers DPROT_AHB_MPU_TABLE_0_REG and DPROT_AHB_MPU_TABLE_1_REG are located in the DPort address space. Only processes with a PID of 0 or 1 can modify these two registers.

**Note (in blue box):**
In hardware, there are three instruction buses corresponding to VAddr1, VAddr2, and VAddr3, respectively. These three buses can initiate load or fetch accesses simultaneously, but only one access is true. If more than one unmasked instruction buses are present, then bit8 of all MMU entries should be set to zero. Otherwise, when an invalid MMU entry is used by an access, the cache will be stalled even if there is no program at this access.

**Subsection Title:**
4.3.2.2 External Memory

**Text under Subsection 4.3.2.2:**

Accesses to the external flash and external SPI RAM are done through a cache and are also handled by an MMU. This Cache MMU can apply different mappings, depending on the PID of the process as well as the CPU the process is running on. The MMU does this in a way that is similar to the internal memory MMU, that is, for every page of virtual memory, it has a register detailing which physical page this virtual page should map to. There are differences between when the MMUs governing the internal memory and the Cache MMU, though.

First of all, the Cache MMU has a fixed page size (which is 64 KB for external flash and 32 KB for external RAM) and secondly, instead of specifying access rights in the MMU entries, the Cache MMU has explicit mapping tables for each PID and processor core. The MMU mapping configuration registers will be referred to as 'entries' in the rest of this chapter. These registers are only accessible from processes with a PID of 0 or 1; processes with a PID of 2 to 7 will have to delegate to one of the above-mentioned processes to change their MMU settings.

The MMU entries, as stated before, are used for mapping a virtual memory page access to a physical memory page access. The MMU controls five regions of virtual address space, detailed in Table 4.3-9. VAddr1 to VAddr4 are used for accessing external flash, whereas VAddrram is used for accessing external RAM. Note that VAddr4 is a subset of VAddr0.

**Footer:**
Espressif Systems
Page number (centered): 83
Document version and link text at the bottom right corner:
ESP32 TRM (Version 5.6)
Submit Documentation Feedback