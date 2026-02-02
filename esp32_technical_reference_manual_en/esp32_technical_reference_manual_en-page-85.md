**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Body Text:**
special mode to allow processes with a PID of 2 to 7 to read the External Flash via address VAddr1. When the DPOR_PRO_SINGLE_IRAM_ENA bit of register DPOR_PRO_CACHE_CTRL_REG is 1, the MMU enters this special mode for PRO_CPU memory accesses. Similarly, when the DPORT_APP_SINGLE_IRAM_ENA bit of register DPORT_APP_CACHE_CTRL_REG is 1, the APP_CPU accesses memory using this special mode.

In this mode, the process and virtual address page supported by each configuration entry of MMU are different.
For details please see Table 4.3-12 and 4.3-13. As shown in these tables, in this special mode VAddr2 and VAddr3 cannot be used to access External Flash.

**Tables:**

**Table Title:** 
Table 4.3-12. MMU Entry Numbers for PRO_CPU (Special Mode)

| VAddr | Count | First MMU entry for PID |
|-------|-------|-------------------------|
| VAddr0 | 64    | -                       |
| VAddr1 | 64    | 0                       |
| VAddr2 | 64    | 256                     |
| VAddr3 | 64    | 384                     |
| VAddr4 | 64    | 512                     |
|       |       | 640                     |
|       |       | 768                     |
|       |       | 896                     |

**Table Title:** 
Table 4.3-13. MMU Entry Numbers for APP_CPU (Special Mode)

| VAddr | Count | First MMU entry for PID |
|-------|-------|-------------------------|
| VAddr0 | 64    | -                       |
| VAddr1 | 64    | 2048                    |
| VAddr2 | 64    | 2304                    |
| VAddr3 | 64    | 2432                    |
| VAddr4 | 64    | 2560                    |
|       |       | 2688                    |
|       |       | 2816                    |
|       |       | 2944                    |

**Examples:**

Example. A PRO_CPU process, with a PID of 1, needs to read external flash address 0x07_2375 via virtual address 0x3F70_2375.
The MMU is not in the special mode.

- According to Table 4.3-9, virtual address 0x3F70_2375 resides in the 0x30th page of .VAddr0
- The modified MMU entry for VAddr0 PID O/1 for the PRO_CPU starts at 0.
- Address 0x07_2375 resides in the 7th 64 KB-sized page.

MMU entry 0x30 needs to be set to 7 and marked as valid by setting the 8th bit to 0. Thus, 0x007 is written to MMU entry 0x30.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32 TRM (Version 5.6)