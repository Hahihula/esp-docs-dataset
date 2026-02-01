**Title: Functional Description**

---

### System

This section describes the core of the chip’s operation, covering its microprocessor, memory organization, system components, and security features.

#### 4.1 Microprocessor and Master

This subsection describes the core processing units within the chip and their capabilities.

##### Subsection Title: High-Performance CPU (4.1.1)

The ESP-RISC-V CPU is a high-performance 32-bit core based on the RISC-V instruction set architecture, comprising base integer instructions, multiplication/division operations, atomic operations, compressed standard extensions etc..

**Feature List**
- Four-stage pipeline that supports an operating clock frequency up to 160 MHz
- RV32IMAC ISA (instruction set architecture)
- Compatible with RISC-V ISA Manual Volume I: Unprivileged ISA Version 2.2 and RISC-V ISA Manual, Volume II: Privileged Architecture, Version 1.10
- Zero wait cycle access to on-chip SRAM and Cache for program and data access over IRAM/DRAM interface
- Branch target buffer (BTB) with static branch prediction
- User mode support along with interrupt delegation
- Interrupt controller with up to 28 external vectored interrupts for both M and U modes, each having programmable priority levels.
- Core local interrupts dedicated for privilege mode 
- Debug module compliant with the specification RISC-V External Debug Support Version 0.13 including JTAG/USB port support

**Note:** For details on instruction trace see Section [4.1.2](#) RISC-V Trace Encoder.

---

#### Subsection Title: RISC-V Trace Encoder (4.1.1.2)

The ESP32-C6 chip provides a way to capture detailed trace information from the High-Performance CPU’s execution, enabling deeper analysis and optimization of the system by connecting it directly with the high-performance CPU's execution unit.

---

**Footer:**  
Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32-C6 Series Datasheet v1.4

--- 

(Note: The text in blue is a hyperlink to another section or document.)