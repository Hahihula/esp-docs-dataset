**Chapter Title:**
Chapter 4 System and Memory

**Figure Caption (with diagram):**
Figure 4-2-1 illustrates the system structure and address mapping.

**Diagram Description in Figure 4.2-1:** 
The figure shows a block diagram of an embedded memory management unit with various components such as Cache, MMU, External memory, ROM, SRAM, GDMA, RTC SLOW Memory, RTC Peripheral, RTC FAST Memory etc., connected through Data bus and Instruction bus.

**Text Below Diagram:**
Figure 4.2-1 System Structure and Address Mapping

**Note Section (in a box):**
- The address space with gray background is not available to users.
- The memory or peripheral marked with a red pentagram can be accessed by the ULP co-processor.
- The range of addresses available in the address space may be larger than the actual available memory of a particular type.

**Subsection Title:**
4.3 Functional Description

**Sub-subsection Title and Content (4.3.1 Address Mapping):**
4.3.1 Address Mapping
The system contains two Harvard Architecture Xtensa® LX7 CPUs, and both can access the same range of address space.
Addresses below 0x4000_0000 are accessed using the data bus. Addresses in the range of 0x4000_0000 ~ 0xFFFF_FFFF are accessed using the instruction bus. Addresses over including 0x5000_0000 are shared by both data bus and instruction bus.
Both data bus and instruction buses are little-endian. The CPU can access data via the data bus using

**Footer:**
Espressif Systems
401 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback