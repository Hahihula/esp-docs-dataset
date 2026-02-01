**Title: Functional Description**

---

### **4.1.1.2 RISC-V Trace Encoder**

The RISC-V Trace Encoder in the ESP32-H2 chip provides a way to capture detailed trace information from the CPU’s execution, enabling deeper analysis and optimization of the system. It connects to the CPU's instruction trace interface and compresses the information into smaller packets, which are then stored in internal SRAM.

**Feature List**
- Compatible with RISC-V Processor Trace Version 1.0
- Arbitrary address range of the trace memory size
- Two synchronization modes:
  - Synchronization counter counts by packet
  - Synchronization counter counts by cycle
- Trace lost status to indicate packet loss
- Automatic restart after packet loss
- Configurable memory writing mode: loop mode or non-loop mode
- FIFO (128 x 8 bits) to buffer packets

For details, see [ESP32-H2 Technical Reference Manual > Chapter RISC-V Trace Encoder (TRACE)](#).

---

### **4.1.1.3 GDMA Controller**

The GDMA Controller is a General Direct Memory Access (GDMA) controller that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer without the CPU’s intervention. The GDMA has six independent channels, three transmit and three receive. These channels are shared by peripherals with the GDMA feature, such as SPI2, UHCI (UART0/UART1), I2S, AES, SHA, ADC, and PARLIO.

**Feature List**
- AHB bus architecture
- Programmable length of data to be transferred in bytes
- Linked list of descriptors for efficient data transfer management
- INCR burst transfer when accessing internal RAM for improved performance
- Access to an address space of up to 324 KB in internal RAM
- Software-configurable selection of peripheral requesting service
- Fixed-priority and round-robin channel arbitration schemes for managing bandwidth
- Support for Event Task Matrix

For details, see [ESP32-H2 Technical Reference Manual > Chapter GDMA Controller (DMA)](#).

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback  
Page 27 ESP32-H2 Series Datasheet v1.2