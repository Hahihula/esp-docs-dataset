**Title: Functional Description**

---

### **4 System**
This section describes the core of the chip’s operation, covering its microprocessor, memory organization, system components, and security features.

#### 4.1 Microprocessor and Master

This subsection describes the core processing units within the chip and their capabilities.

##### Subsection Title:
**4.1.1 High-Performance CPU**

The ESP-RISC-V CPU (HP CPU) is a high-performance 32-bit core based on the RISC-V instruction set architecture (ISA) comprising base integer (I), multiplication/division (M), atomic (A) and compressed (C) standard extensions.

**Feature List**
- Five-stage pipeline that supports an operating clock frequency up to 160 MHz
- **RV32IMAC ISA** (instruction set architecture)
- Zc extensions (Zcb, Zcmp, and Zcmct)
- Two-cycle pipelined multiplier and radix-4 SRT divider
- Compatible with RISC-V ISA Manual Volume I: Unprivileged ISA Version 2.2 and RISC-V ISA Manual, Volume II: Privileged Architecture, Version 1.10
- Zero wait cycle access to on-chip SRAM and cache for program and data access over IRAM/DRAM interface
- Branch predictor BHT, BTB, and RAS
- Compliant with RISC-V Core Local Interrupt (CLINT)
- Compliant with RISC-V Core-Local Interrupt Controller (CLIC)
- Two privilege modes: Machine (M) mode and User (U) mode
- Debug module (DM) compliant with the specification RISC-V External Debug Support Version 0.13 with external debugger support over an industry-standard JTAG/USB port
- Offline trace debug compliant with RISC-V Trace Specification v2.0, see Section **4.1.1.2 RISC-V Trace Encoder**
- Hardware trigger compliant with the specification RISC-V External Debug Support Version 0.13 with up to three breakpoints/watchpoints
- Physical memory protection (PMP) and attributes (PMA) for up to 16 configurable regions

---

**Footer:**
Espressif Systems  
Page number: **31**  
Document title: ESP32-C61 Series Datasheet v0.5