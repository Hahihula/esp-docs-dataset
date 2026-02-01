**Title: Functional Description**

---

### System

This section describes the core of the chip’s operation, covering its microprocessor, memory organization, system components, and security features.

#### 4.1 Microprocessor and Master

This subsection describes the core processing units within the chip and their capabilities.

##### 4.1.1 ESP-RISC-V CPU

The ESP-RISC-V CPU is a 32-bit core based on the RISC-V instruction set architecture (ISA) comprising base integer (I), multiplication/division (M), atomic (A), and compressed (C) standard extensions.

**Feature List**
- Four-stage pipeline that supports an operating clock frequency of up to 96 MHz
- **RV32IMAC ISA** (instruction set architecture)
- Compatible with RISC-V A Manual Volume I: Unprivileged ISA Version 2.2 and RISC-V ISA Manual, Volume II: Privileged Architecture, Version 1.10
- Zero wait cycle access to on-chip SRAM and cache for program and data access over IRAM/DRAM interface
- Branch target buffer (BTB) with static branch prediction
- User (U) mode support along with interrupt delegation
- Interrupt controller with up to 28 external vectored interrupts for both M and U modes with 16 programmable priority and threshold levels
- Core local interrupts (CLINT) dedicated for machine mode and user mode
- Debug module (DM) compliant with the specification RISC-V External Debug Support Version 0.13 with external debugger support over an industry-standard JTAG/USB port
- Support for instruction trace, see Section **4.1.2 RISC-V Trace Encoder**
- Debugger with a direct system bus access (SBA) to memory and peripherals
- Hardware trigger compliant to the specification RISC-V External Debug Support Version 0.13 with up to 4 breakpoints/watchpoints
- Physical memory protection (PMP) and attributes (PMA) for up to 16 configurable regions
- 32-bit AHB system bus for peripheral access
- Configurable events for core performance metrics

For details, see **ESP32-H2 Technical Reference Manual** > Chapter ESP-RISC-V CPU.

---

Espressif Systems  
Submit Documentation Feedback  

Page: 26  
Document Version: v1.2