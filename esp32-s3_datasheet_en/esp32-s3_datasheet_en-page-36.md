**Title: Functional Description**

---

### System

This section describes the core of the chip’s operation, covering its microprocessor, memory organization, system components, and security features.

#### 4.1 Microprocessor and Master

This subsection describes the core processing units within the chip and their capabilities.

##### CPU (4.1.1)

ESP32-S3 has a low-power Xtensa® dual-core 32-bit LX7 microprocessor.
- **Feature List**
  - Five-stage pipeline that supports the clock frequency of up to 240 MHz
  - 16-bit/24-bit instruction set providing high code density
  - 32-bit customized instruction set and 128-bit data bus that provide high computing performance
  - Support for single-precision floating-point unit (FPU)
  - 32-bit multiplier and 32-bit divider
  - Unbuffered GPIO instructions
  - 32 interrupts at six levels
  - Windowed ABI with 64 physical general registers
  - Trace function with TRAX Compressor, up to 16 KB trace memory
  - JTAG for debugging

For information about the Xtensa® Instruction Set Architecture (ISA) Summary:
- [Xtensa® Instruction Set Architecture (ISA) Summary](#)

---

#### Processor Instruction Extensions (PIE) (4.1.2)

ESP32-S3 contains a series of new extended instruction set in order to improve the operation efficiency of specific AI and DSP (Digital Signal Processing) algorithms.
- **Feature List**
  - 128-bit new general-purpose registers
  - 128-bit vector operations, e.g., complex multiplication, addition, subtraction, multiplication, shifting, comparison, etc
  - Data handling instructions and load/store operation instructions combined
  - Non-aligned 128-bit vector data

---

**Footer:**
- Espressif Systems
- Page number: 36
- Document title: ESP32-S3 Series Datasheet v2.1
- Link to submit documentation feedback:
  - [Submit Documentation Feedback](#)