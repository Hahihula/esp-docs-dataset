**Title:**
4 Functional Description

**Diagram Title and Caption:**
Figure 4-1. Address Mapping Structure

**Subsection Heading with Subheading (with text):**
4.1.3.1 System and Memory

**Body Text under "Internal Memory":**

ESP32-P4's internal memory includes:
- **128 KB of HP ROM:** 200 MHz, for HP CPU booting and core functions
- **768 KB of HP L2MEM:** 200 MHz, for HP CPU data and instructions
- **16 KB of LP ROM:** 40 MHz, for LP CPU booting and core functions
- **32 KB of LP SRAM:** 40 MHz, for LP CPU data and instructions
- **4 Kbit of eFuse:** 1792 bits are reserved for user data, such as encryption key and device ID
- **8 KB of SPM (Scratchpad Memory):** 360 MHz, for HP CPU fast access

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6