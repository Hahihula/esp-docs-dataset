**Title: Functional Description**

---

### CPU and Memory

#### Subtitle: CPU (4.1)

ESP32 contains one or two low-power Xtensa® 32-bit LX6 microprocessor(s) with the following features:

- **7-stage pipeline to support the clock frequency of up to 240 MHz** (160 MHz for ESP32-SOWD [NRND])
- **16/24-bit Instruction Set provides high code-density**
- Support for Floating Point Unit
- Support for DSP instructions, such as a 32-bit multiplier, a 32-bit divider, and a 40-bit MAC
- Support for 32 interrupt vectors from about 70 interrupt sources

The single-/dual-CPU interfaces include:

- Xtensa RAM/ROM Interface for instructions and data
- Xtensa Local Memory Interface for fast peripheral register access
- External and internal interrupt sources
- JTAG for debugging

For information about the Xtensa® Instruction Set Architecture, please refer to [Xtensa® Instruction Set Architecture (ISA) Summary](#).

#### Subtitle: Internal Memory (4.1.2)

ESP32’s internal memory includes:

- **448 KB of ROM** for booting and core functions
- 520 KB of on-chip SRAM for data and instructions
- 8 KB of SRAM in RTC, which is called RTC FAST Memory and can be used for data storage; it is accessed by the main CPU during RTC Boot from the Deep-sleep mode.
- **8 KB of SRAM** in RTC, which is called RTC SLOW Memory and can be accessed by the ULP coprocessor during the Deep-sleep mode.

1 Kbit of eFuse: 256 bits are used for the system (MAC address and chip configuration) and the remaining 768 bits are reserved for customer applications, including flash-encryption and chip-ID.
- In-package flash or PSRAM

**Note:** Products in the ESP32 series differ from each other, in terms of their support for in-package flash or PSRAM and the size of them. For details, please refer to Section 1 [ESP32 Series Comparison](#).

---

Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32 Series Datasheet v5.2

--- 

(Note: The text contains references marked as `[link]` which are not provided in the image.)