**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MMU PR)

**Table Header:**
Task 4-3-6. Page Boundaries for SRAM2 MMU

| Pages | Bottom       | Top         |
|-------|-------------|------------|
| 8 KB Pages | -          |            |
| 4 KB Pages | -          |            |
| 2 KB Pages | -          |            |

**Table Content:**
- **Page:** 
  - Page numbers from `0` to `15`
  
- **Bottom and Top:**
  - Each row contains a pair of hexadecimal values for the bottom and top addresses.

**Example Entries in Table (partial):**
```
| Bottom       | Top         |
|-------------|------------|
| 3FFC000     | 3FFC1FFF   |
| 3FFC2000    | 3FFC3FFF   |
| ...         | ...        |
```

**Subsection Title:**
MMU Mapping

**Body Text under MMU Mapping:**
For each of the SRAMO and SRAM2 MMUs, access rights and virtual to physical page mapping are done by a set of 16 registers. In contrast to most of the other MMUs, each register controls a **physical page**, not a virtual one. These registers control which of the PIDs have access to the physical memory, as well as which virtual page maps to this physical page.

The bits in the register are described in Table 4-3-7. Keep in mind that these registers only govern accesses from processes with PID 2 to 7; PID 0 and 1 always have full read and write access to all pages and no virtual-to-physical mapping is done. In other words, if a process with a PID of 0 or 1 accesses **virtual page x**, the access will always go to physical page `x`, regardless of these register settings.

These registers, as well as the page size selection registers DPORT_IMMU_PAGE_MODE_REG and DPORT_DMMU_PAGE_MODE_REG, are only writable from a process with PID 0 or 1. 

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback