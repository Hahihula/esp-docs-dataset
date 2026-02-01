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
- five-stage pipeline that supports clock frequency of up to 240 MHz
- **RV32IMAC ISA** (instruction set architecture)
- two-cycle pipelined multiplier and radix-4 SRT divider
- Zc extensions (Zcb, Zcmp and Zcmt)
- custom hardware loop instructions (Xhwip)
- compliant with RISC-V Core Local Interrupt (CLINT)
- compliant with RISC-V Core-Local Interrupt Controller (CLIC)
- branch predictor BHT, BTB, and RAS
- up to 3 hardware breakpoints/watchpoints
- up to 16 PMP/PMA regions
- Machine and User privilege modes
- USB/JTAG for debugging
- compliant with RISC-V debug specification v0.13
- offline trace debug that is compliant with RISC-V Trace Specification v2.0

For details, see **ESP32-C5 Technical Reference Manual** > Chapter High-Performance CPU.

---

### 4.1.2 RISC-V Trace Encoder

The RISC-V Trace Encoder in the ESP32-C5 chip provides a way to capture detailed trace information from the High-Performance CPU’s execution, enabling deeper analysis and optimization of the system. It connects to the HP CPU's instruction trace interface and compresses the information into smaller packets, which are then stored in internal SRAM.

---

**Footer:**
Espressif Systems  
34  
Submit Documentation Feedback

ESP32-C5 Series Datasheet v1.0