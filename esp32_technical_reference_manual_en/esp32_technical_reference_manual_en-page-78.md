**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Body Text:**
converted to a read from or write to the exact same physical page. This allows an operating system, running under PID 0 and/or 1, to always have access to the entire physical memory range.

For PID 2 to 7, however, every virtual page can be reconfigured, on a per-PID basis, to map to a different physical page. This way, reads and writes to an offset within a virtual page get translated into reads and writes to the same offset within a different physical page. This is illustrated in Figure 4.3-1: the CPU (running a process with a PID between 2 to 7) tries to access memory address Ox3FFC_2345. This address is within the virtual Page 1 memory region, at offset Ox0345. The MMU is instructed that for this particular PID, it should translate an access to virtual page 1 into physical Page 2. This causes the memory access to be redirected to the same offset as the virtual memory access, yet in Page 2, which results in the effective access of physical memory address Ox3FFC_4345. The page size in this example is 8 KB.

**Figure Caption:**
Figure 4.3-1. MMU Access Example

**Table Title and Content:**
Table 4.3-4. Page Mode of MMU for the Remaining 128 KB of Internal SRAM0 and SRAM2
| DPORT_IMMU_PAGE_MODE | DPORT_DMMU_PAGE_MODE | Page size |
|------------------------|-----------------------|-----------|
| 0                      | 0                     | 8 KB      |
| 1                      | 1                     | 4 KB      |
| 2                      | 2                     | 2 KB      |

**Subsection Title:**
Non-MMU Governed Memory

**Body Text for Subsection:**
For the MMU-managed region of SRAM0 and SRAM2, the page size is configurable as 8 KB, 4 KB and 2 KB. The configuration is done by setting the DPORT_IMMU_PAGE_MODE (for SRAM0) and DPORT_DMMU_PAGE_MODE (for SRAM2) bits in registers DPORT_IMMU PAGE_MODE_REG and DPORT_DMMU_PAGE_MODE REGARDING, as detailed in Table 4.3-4. Because the number of pages for either region is fixed at 16, the total amount of memory covered by these pages is 128 KB when 8 KB pages are selected, 64 KB when 4 KB pages are selected, and 32 KB when 2 KB pages are selected. This implies that for 8 KB pages, the entire MMU-managed range is used, but for the other page sizes there will be a part of the 128 KB memory that will not be governed by the MMU settings. Concretely, for a page size of 4 KB, these regions are Ox4009_0000 to Ox4009_FFFF and Ox3FFD_0000 to Ox3FFD_FFFF; for a page size of 2 KB, the regions are Ox4008_8000 to Ox4009_FFFF and Ox3FFC_8000 to Ox3FFD_FFFF. These ranges are readable and writable by processes with a PID of 0 or 1; processes with other PIDs cannot access this memory.

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Page Numbering:**
78 ESP32 TRM (Version 5.6)