**Title: Functional Description**

---

### System

This section describes the core of the chip’s operation, covering its microprocessor, memory organization, system components, and security features.

#### Microprocessor and Master (4.1.1)

This subsection describes the core processing units within the chip and their capabilities.
##### High-Performance CPU (4.1.1.1)
ESP32-C3 has a low-power 32-bit RISC-V single-core microprocessor with the following features:
- four-stage pipeline that supports a clock frequency of up to 160 MHz
- RV32IMC ISA
- 32-bit multiplier and 32-bit divider
- up to 32 vectored interrupts at seven priority levels
- up to 8 hardware breakpoints/watchpoints
- up to 16 PMP regions
- JTAG for debugging

For details, see [ESP32-C3 Technical Reference Manual > Chapter High-Performance CPU](#).

#### GDMA Controller (4.1.1.2)
ESP32-C3 has a general DMA controller (GDMA) with six independent channels, i.e., three transmit channels and three receive channels. These six channels are shared by peripherals with DMA feature. The GDMA controller implements a fixed-priority scheme among these channels, whose priority can be configured.

The GDMA controller controls data transfer using linked lists. It allows peripheral-to-memory and memory-to-memory data transfer at a high speed. All channels can access internal RAM.
Peripherals on ESP32-C3 with DMA feature are SPI2, UHCI0, I2S, AES, SHA, and ADC.

For details, see [ESP32-C3 Technical Reference Manual > Chapter GDMA Controller (DMA)](#).

#### Memory Organization (4.1.2)
This subsection describes the memory arrangement to explain how data is stored, accessed, and managed for efficient operation.
Figure 4-1 illustrates the address mapping structure of ESP32-C3.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

ESP32-C3 Series Datasheet v2.2