**Title:**
4 Functional Description

**Subtitle and Section Heading:**
4.1.2 Memory Organization

**Body Text:**
This subsection describes the memory arrangement to explain how data is stored, accessed, and managed for efficient operation.

Figure 4-1 illustrates the address mapping structure of ESP32-S3.

**Diagram Labels (from top-left clockwise):**

- CPU
  - Address ranges:
    - `0x0000_0000`
    - `0x3BFF_FFFF`
    - `0x3C00_0000`
    - `0x3DFF_FFFF`
    - `0x3E00_0000`
    - `0x3FCB_FFFF`
    - `0x3F80_0000`
    - `0x3FCF_FFFF`
    - `0x3FD0_0000`
    - `0x3FEF_FFFF`
    - `0x3FF0_0000`
    - `0x3FF1_FFFF`

- ROM
  - Address ranges:
    - `0x2FF2_0000`
    - `0x4000_0000`
    - `0x4005_FFFF`
    - `0x4006_0000`
    - `0x4036_FFFF`
    - `0x4037_0000`
    - `0x403D_FFFF`
    - `0x41FF_0000`
    - `0x4200_0000`
    - `0x43FF_FFFF`

- SRAM
  - Address ranges:
    - `0x5000_0000`
    - `0x5001_FFFF`
    - `0x5000_2000`
    - `0x5F00_0000`
    - `0x6000_0000`
    - `0x6D00_0FFF`
    - `0x600F_E000`
    - `0x6010_0000`

- GDMA
  - Address ranges:
    - Not specified

**Diagram Labels (bottom-left clockwise):**

- External Memory -> MMU -> Cache -> ROM, SRAM connections.
- RTC Slow Memory: 
  - Address range not fully visible but includes `0x4000_0000` to possibly higher addresses.

**Legend in Diagram:**
- Gray background indicates "Not available for use"
- White area with text indicating address ranges

**Figure Caption and Note:**

**Figure caption:** Figure 4-1. Address Mapping Structure

**Note:** The memory space with gray background is not available to users.

**Footer Information:**
Espressif Systems
38 ESP32-S3 Series Datasheet v2.1 Submit Documentation Feedback