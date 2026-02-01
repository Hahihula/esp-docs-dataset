**Title:**
4 Functional Description

**Figure Title and Caption:**
- **Figure:** Figure 4-1. Address Mapping Structure.

**Note Box Content (in blue):**
The memory space with gray background is not available for use.

**Subtitle:**
4.1.2.1 Internal Memory

**Body Text:**
ESP32-S2’s internal memory includes:

- *128 KB of ROM*: for booting and core functions
- *320 KB of on-chip SRAM*: 1 MB data and instructions, running at a configurable frequency of up to 240 MHz.
- *RTC FAST Memory*: 8 KB of SRAM in RTC. It can be accessed by the main CPU. It can retain data in Deep-sleep mode.
- *RTC SLOW Memory*: 8 KB of SRAM in RTC. It can be accessed by the main CPU or the co-processor. It can retain data in Deep-sleep mode.
- *4 Kbit of eFuse*: 1792 bits are reserved for user data, such as encryption key and device ID.

**Additional Information:**
In-package flash and PSRAM:
See details in Chapter [ESP32-S2 Series Comparison](#) ESP32-S2 Technical Reference Manual > Chapter System and Memory

For more information, please refer to:

- **Link:** ESP32-S2 Technical Reference Manual
- **Text:** Chapter System and Memory.

**Footer:**
Espressif Systems  
Page 34  
Submit Documentation Feedback  
ESP32-S2 Series Datasheet v1.8