**Title: Functional Description**

---

### **4.1.1.2 RISC-V Trace Encoder**

The RISC-V Trace Encoder in the ESP32-C61 chip provides a way to capture detailed trace information from the High-Performance CPU’s execution, enabling deeper analysis and optimization of the system. It connects to the HP CPU's instruction trace interface and compresses the information into smaller packets, which are then stored in internal SRAM.

**Feature List**
- Compatible with Efficient Trace for RISC-V Version 2.0
- Synchronization packets sent every few clock cycles or packets
- Zero bytes as anchor tags to identify boundaries between data packets
- Configurable memory writing mode: loop mode or non-loop mode
- Trace lost status to indicate packet loss
- Automatic restart after packet loss
- Support for delta address mode and full address mode
- Support for filter unit

---

### **4.1.3 GDMA Controller**

The GDMA Controller is a General Direct Memory Access (GDMA) controller that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer without the CPU’s intervention. The GDMA has four independent channels, two transmit channels and two receive channels. These channels are shared by peripherals with the GDMA feature, such as SPI2, I2S, SHA, and ADC.

**Feature List**
- Programmable length of data to be transferred in bytes
- Linked list of descriptors for efficient data transfer management
- INCR burst transfer when accessing internal RAM for improved performance
- Access to internal RAM and off-package PSRAM
- Software-configurable selection of peripheral requesting service
- Fixed-priority and round-robin channel arbitration schemes for managing bandwidth
- Support for Event Task Matrix

---

### **4.1.2 Memory Organization**

This subsection describes the memory arrangement to explain how data is stored, accessed, and managed for efficient operation.

**Figure 4-1 illustrates the address mapping structure of ESP32-C61.**

Espressif Systems  
Page: 32  
ESP32-C61 Series Datasheet v0.5