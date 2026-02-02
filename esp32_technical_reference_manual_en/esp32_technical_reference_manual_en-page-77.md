**Chapter Title:**
Chapter 4 Memory Management and Protection Units (MMU, MPU)

**Body Text:**

or 1, the memory can be read (and written when it is RAM) using the addresses specified in Table 4.3-1. When it is 2 ~ 7, the memory cannot be accessed.

**Subheading:** RTC FAST & RTC SLOW MPU

The 8 KB RTC FAST Memory as well as the 8 KB of RTC SLOW Memory are governed by two configurable MPUs. The MPUs can be configured to allow or deny access to each individual PID, using the RTC_CNTL_RTC_PID_.

CONFIG_REG and DPORT_AHBLITE_MPU_TABLE_RTC_REG registers. Setting a bit in these registers will allow the corresponding PID to read or write from the memory; clearing the bit disables access. Access for PID 0 and 1 to RTC SLOW memory cannot be configured and is always enabled. Table 4.3-2 and 4.3-3 define the bit-to-PID mappings of the registers.

**Table Title:** Table 4.3-2. MPU for RTC FAST Memory

| Size | Boundary address Low | Authority PID | High |
|------|-----------------------|---------------|------|
| 8 KB | 0x3FF8_0000           | RTC_CNTL_RTC_PID_CONFIG bit   | 1 2 3 4 5 6 7 |
| 8 KB | 0x400C_0000           | RTC_CNTL_RTC_PID_CONFIG bit   | 1 2 3 4 5 6 7 |

**Table Title:** Table 4.3-3. MPU for RTC SLOW Memory

| Size | Boundary address Low High PID = 0/1 Authority PID |
|------|---------------------|-----------|---------|
| 8 KB | 0x5000_0000        | DPORT_AHBLITE_MPU_TABLE_RTC_REG bit Read/Write | 0 1 2 3 4 5 |

Register RTC_CNTL_RTC_PID_CONFIG_REG is part of the RTC peripheral and can only be modified by processes with a PID of 0; register DPORT_AHBLITE_MPU_TABLE_RTC_REG is a Dport register and can be changed by processes with a PID of 0 or 1.

**Subheading:** SRAMO and SRAM2 upper 128 KB MMUs

Both the upper 128 KB of SRAMO and the upper 128 KB of SRAM2 are governed by an MMU. Not only can these MMUs allow or deny access to the memory they govern (just like the MPUs do), but they are also capable of translating the address a CPU reads from or writes to (which is a virtual address) to a possibly different address in memory (the physical address).

In order to accomplish this, the internal RAM MMUs divide the memory range they govern into 16 pages. The page size is configurable as 8 KB, 4 KB and 2 KB. When the page size is 8 KB, the 16 pages span the entire 128 KB memory region; when the page size is 4 KB or 2 KB, a non-MMU-covered region of 64 or 96 KB, respectively, will exist at the end of the memory space. Similar to the virtual and physical addresses, it is also possible to imagine the pages as having a virtual and physical component. The MMU can convert an address within a virtual page to an address within a physical page.

For PID 0 and 1, this mapping is 1-to-1, meaning that a read from or write to a certain virtual page will always be

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
77 Submit Documentation Feedback