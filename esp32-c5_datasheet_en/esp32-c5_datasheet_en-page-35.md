**Title: Functional Description**

---

### Feature List

- compatible with Efficient Trace for RISC-V Version 2.0
- synchronization packets sent every few clock cycles or packets
- zero bytes as anchor tags to identify boundaries between data packets
- configurable memory writing mode: loop mode or non-loop mode
- trace lost status to indicate packet loss
- automatic restart after packet loss
- support for delta address mode and full address mode
- Support for filter unit

For details, see [ESP32-C5 Technical Reference Manual > Chapter RISC-V Trace Encoder (TRACE)](#).

---

**Subtitle: 4.11.3 Low-Power CPU**

The ESP32-C5 Low-Power CPU (LP CPU) is a 32-bit processor based on the RISC-V ISA comprising integer (I), multiplication/division (M), atomic (A), and compressed (C) standard extensions. It is designed for ultra-low power consumption and is capable of staying powered during Deep-sleep mode when the HP CPU is powered down.

This LP CPU is designed as a simplified, low-power replacement of HP CPU in sleep modes. It can be also used to supplement the functions of the HP CPU in normal working mode. The LP CPU and LP memory remain powered on in Deep-sleep mode. Hence, the developer can store a program for the LP CPU in the LP memory to access LP IO, LP peripherals, and RTC timers in Deep-sleep mode.

---

### Feature List

- two-stage pipeline that supports a clock frequency of up to 48 MHz
- [RV32IMAC ISA](#) (instruction set architecture)
- 3-4 cycle multiplier and iterative divider
- support for custom vectored interrupts
- up to 2 hardware breakpoints/watchpoints
- JTAG for debugging
- compliant with RISC-V debug specification v0.13
- boot by the CPU, its dedicated timer, or LP IO

For details, see [ESP32-C5 Technical Reference Manual > Chapter Low-Power CPU](#).

---

**Subtitle: 4.11.4 GDMA Controller**

The GDMA Controller is a General Direct Memory Access (GDMA) controller that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer without the CPU’s intervention. The GDMA has six independent channels, three transmit channels and three receive channels. These channels are shared by peripherals with the GDMA feature, consisting of SPI2, UHCI0, I2S, AES, SHA, ADC, and PARLIO.

---

**Footer:**
Espressif Systems  
35  
[Submit Documentation Feedback](#)  

ESP32-C5 Series Datasheet v1.0