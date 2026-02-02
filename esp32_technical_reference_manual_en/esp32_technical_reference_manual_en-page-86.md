**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**GoBack**

**Example Section:**
- **Title:** Example 2.
- **Content:** An APP_CPU process, with a PID of 4, needs to read external flash address 0x44_048C via virtual address 0x4044_048C. The MMU is not in special mode.

**Subsection:**
- **Title:** According to Table
- **Content:** 
  - "According to Table 4.3-9, virtual address 0x4044_048C resides in the OX4th page of VAddr2."
  - "According to Table 4.3-11, the MMU entry for VAddr2 for the APP_CPU starts at 2560."

**Subsection:**
- **Title:** The modified MMU entry is
- **Content:** 
  - Address 0x44_048C resides in the OX4th's 64 KB-sized page.
  
**Subsection:**
- **Title:** MMU entry needs to be set and marked as valid by setting the Sth bit to 0. Thus, Ox044 is written to MMU entry 2564.

**Section Title: External RAM**

**Body Text:**
Processes running on PRO_CPU and APP_CPU can read and write External SRAM via the Cache at virtual address range VAddrRAM, which is 0x3F80_0000 ~ 0x3FBF_FFFF. As with the flash MMU, the address space and the physical memory are divided into pages. For the External RAM MMU, the page size is 32 KB and the MMU is able to map 256 physical pages into the virtual address space, allowing for 32 KB x 256 = 8 MB of physical external RAM to be mapped.

The mapping of virtual pages into this memory range depends on the mode this MMU is in: Low-High mode. Even-Odd mode or Normal mode In all cases; The DPORT_PRO_DRAM_HL bit and DPORT_PRO_DRAM_SPLIT bit in register DPORT_PRO_CACHE_CTRL_REG, the DPORT_APP_DRAM_HL bit and DPORT_APPDRAM_SPLIT bit in register DPORT_APP_CACHE_CTRL_REG determine the virtual address mode for External SRAM. For details, please see Table 4.3-14.

If a different mapping for the PRO_CPU and APP_CPU is required; The Normal Mode should be selected as it's only that can provide this If It Is allowable for the PRO_CPU and the APP_CPU to share the same mapping using either High-Low or Even-Odd mode could give speed gain when both CPUs access memory frequently.

In case, the APP_CPU cache is disabled which renders the region of 0x4007_8000 to 0x4007_FFFF usable as normal internal RAM; The usability of various code modes changes. Normal mode will allow PRO_CPU access to external RAM to keep functioning but the APP_CPU will be unable to access the external RAM.

High-Low mode allows both CPUs use external RAM, But only for the 2 MB virtual memory addresses from Ox3F80_0000 to Ox3F9F_FFFF. It is not advised to use Even-Odd mode with the APP_CPU cache region disabled

**Table Title:**
Table 4.3-14. Virtual Address Mode for External SRAM

| Mode       | DPORT_PRO_DRAM_HL | DPORT_PRO_DRAM_SPLIT | DPORT_APPDRAM_SPLIT |
|------------|--------------------|-----------------------|----------------------|
| Low-High   |                   |                       |                      |
| Even-Odd  |                   |                       |                      |
| Normal     |                   |                       |                      |

**Table Description:**
In normal mode, the virtual-to-physical page mapping can be different for both CPUs. Page mappings for PRO_CPU are set using MMU entries for LVAaddrRAM and page mappings for APP_CPU can be configured with the MMU entries for RVaddrRAM.

**Footer Text:** 
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback

**Page Number:**
86