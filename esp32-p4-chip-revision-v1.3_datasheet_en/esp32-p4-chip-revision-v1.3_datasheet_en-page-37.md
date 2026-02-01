**Title: Functional Description**

---

### System

This section describes the core of the chip’s operation, covering its microprocessor, DMA controllers, memory organization, system components, and security features.

#### 4.1 Microprocessor and Master

This subsection describes the core processing units within the chip and their capabilities.

##### Subsection Title: High-Performance CPU

ESP32-P4 has an HP 32-bit RISC-V dual-core processor with the following features:

**Feature List**
- Five-stage pipeline that supports clock frequency of up to 360 MHz
- RV32IMAFC ISA (instruction set architecture)
- Zc extensions (Zcb, Zcmp, and Zcmr)
- Custom AI and DSP extension (XespV)
- Custom hardware loop instructions (XespLoop)
- Compliant with RISC-V Core Local Interrupt (CLINT)
- Compliant with RISC-V Core-Local Interrupt Controller (CLIC)
- Branch predictor BHT, BTB, and RAS
- Up to three hardware breakpoints/watchpoints
- Up to 16 PMP/PMA regions
- Machine and User privilege modes
- USB/JTAG for debugging
- Compliant with RISC-V debug specification v0.13
- Offline trace debug that is compliant with RISC-V Specification v2.0

#### Subsection Title: RISC-V Trace Encoder (TRACE)

The RISC-V Trace Encoder in the ESP32-P4 chip provides a way to capture detailed trace information from the High-Performance CPU’s execution, enabling deeper analysis and optimization of the system. It connects to the HP CPU's instruction trace interface and compresses the information into smaller packets, which are then stored in internal SRAM.

**Feature List**
- Compatible with Efficient Trace for RISC-V v2.0

---

Espressif Systems  
37  
Submit Documentation Feedback  
ESP32-P4 Series Datasheet v0.6