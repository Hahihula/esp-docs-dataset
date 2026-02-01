**Title: Functional Description**

---

### **4.1.1.4 Low-Power CPU**

ESP32-P4 integrates an LP 32-bit RISC-V single-core processor. This LP CPU is designed as a simplified, low-power replacement of HP CPU in sleep modes. It can be also used to supplement the functions of the HP CPU in normal working mode. The LP CPU and LP memory remain powered on in Deep-sleep mode. Hence, the developer can store a program for the LP CPU in the LP memory to access LP IO, LP peripherals, and real-time timers in Deep-sleep mode.

**Feature List**
- Two-stage pipeline that supports a clock frequency of up to 40 MHz
- **RV32IMAC ISA (instruction set architecture)**
- 18 vector interrupts
- Debug module compliant with RISC-V External Debug Support Version 0.13 with external debugger support over an industry-standard JTAG/USB port
- Hardware trigger compliant with RISC-V External Debug Support Version 0.13 with up to 2 breakpoints/watchpoints
- Core performance metric events
- Wake-up interrupt for HP CPU
- Access to HP memory and LP memory
- Access to the entire peripheral address space

---

### **4.1.2 System DMA**

This subsection describes the system DMA.

**Feature List**
- General Direct Memory Access (GDMA) is a feature that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer at high speed. The CPU is not involved in the GDMA transfer and therefore is more efficient with less workload.
  - ESP32-P4 has two types of general-purpose DMA controllers, namely GDMA-AHB and GDMA-AXI, to directly access the AHB bus or the AXI bus respectively.

**Feature List**
- Architecture:
  - **GDMA-AHB:** AHB bus architecture
  - **GDMA-AXI:** AXI bus architecture, which gives the possibility to complete up to eight transactions out of order and up to eight outstanding transactions.
- Programmable length of data to be transferred in bytes
- Access via any address and size

---

**Footer:**
Espressif Systems  
39  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)