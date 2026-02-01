**Title:**
4 Functional Description

**Figure Title and Caption:**
- **Figure:** Figure 4-1.
- **Caption:** Address Mapping Structure

**Note Section (inside a blue box):**
- Note:
  - The memory space with gray background is not available for use.

**Subsection Heading:**
4.1.2.1 Internal Memory

**Body Text under Subsection:**
The internal memory of ESP32-C3 refers to the memory integrated on the chip die or in the chip package, including ROM, SRAM, eFuse, and flash.
- 384 KB of ROM; for booting and core functions
- 400 KB of on-chip SRAM: for data and instructions, running at a configurable frequency of up to 160 MHz. Of the 400 KB SRAM, 16 KB is configured for cache.
- RTC FAST memory: 8 KB of SRAM that can be accessed by the main CPU. It can retain data in Deep-sleep mode
- 4 Kbit of eFuse: 1792 bits are reserved for your data, such as encryption key and device ID

**Footer Information (inside a blue box):**
Espressif Systems  
34 Submit Documentation Feedback ESP32-C3 Series Datasheet v2.2