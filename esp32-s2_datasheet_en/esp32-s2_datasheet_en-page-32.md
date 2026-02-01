**Title: Functional Description**

---

### System

This section describes the core of the chip’s operation, covering its microprocessor, memory organization, system components, and security features.

#### 4.1 Microprocessor and Master

This subsection describes the core processing units within the chip and their capabilities.

##### CPU (4.1.1)

ESP32-S2 contains one low-power Xtensa® 32-bit LX7 microprocessor with the following features:

- **7-stage pipeline** that supports the clock frequency of up to 240 MHz
- **16/24-bit Instruction Set providing high code-density**
- support for *32-bit multiplier* and *32-bit divider*
- unbuffered GPIO instructions
- support for *32 interrupts at six levels*
- support for windowed ABI with *64 physical general registers*
- support for trace function with TRAX compressor, up to 16 KB trace memory

JTAG for debugging.

For information about the Xtensa® Instruction Set Architecture, please refer to [Xtensa® Instruction Set Architecture (ISA) Summary](#).

---

#### ULP Coprocessor (4.1.2)

The ULP co-processor is designed as a simplified, low-power replacement of CPU in sleep modes. It can be also used to supplement the functions of the CPU in normal working mode. The ULP co-processor and RTC memory remain powered on during the Deep-sleep mode. Hence, the developer can store a program for the ULP co-processor in the RTC slow memory to access RTC GPIO, RTC peripheral devices, RTC timers and internal sensors during the Deep-sleep mode.

ESP32-S2 has two ULP co-processors, with one based on RISC-V instruction set architecture (ULP-RISC-V) and the other on finite state machine (ULP-FSM). The clock of the co-processor is the internal 8 MHz oscillator.

##### Features:

- support for [RV32IMC](#) instruction set
- thirty-two *32-bit general-purpose registers*
- **32-bit multiplier** and divider
- support for interrupts

---

ULP-RISC-V has the following features:
- support for RV32IMC instruction set (cross-referenced)
- thirty-two 32-bit general-purpose registers.
- 32-bit multiplier and divider.

---

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-S2 Series Datasheet v1.8

---