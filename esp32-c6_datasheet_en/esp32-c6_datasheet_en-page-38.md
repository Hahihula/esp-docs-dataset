**Title: Functional Description**

The HP CPU’s instruction trace interface and compresses the information into smaller packets, which are then stored in internal SRAM.

**Feature List**
- Compatible with RISC-V Processor Trace Version 1.0
- Synchronization packets sent every few clock cycles or packets
- Zero bytes as anchor tags to identify boundaries between data packets
- Configurable memory writing mode: loop mode or non-loop mode
- Trace lost status to indicate packet loss
- Automatic restart after packet loss

For details, see [ESP32-C6 Technical Reference Manual > Chapter RISC-V Trace Encoder (TRACE)](#).

**Subtitle 4.11.3 Low-Power CPU**

The ESP32-C6 Low-Power CPU (LP CPU) is a 32-bit processor based on the RISC-V ISA comprising integer (I), multiplication/division (M), atomic (A), and compressed (C) standard extensions. It is designed for ultra-low power consumption and is capable of staying powered on during Deep-sleep mode when the HP CPU is powered down.

**Feature List**
- Two-stage pipeline that supports a clock frequency of up to 20 MHz
- RV32IMAC ISA (instruction set architecture)
- 19 vector interrupts
- Debug module compliant with RISC-V External Debug Support Version 0.13 with external debugger support over an industry-standard JTAG/USB port
- Hardware trigger compliant with RISC-V External Debug Support Version 0.13 with up to 2 breakpoints/watchpoints
- 32-bit AHB system bus for peripheral and memory access
- Core performance metric events
- Able to wake up the HP CPU and send an interrupt to it
- Access to HP memory and LP memory
- Access to the entire peripheral address space

For details, see [ESP32-C6 Technical Reference Manual > Chapter Low-Power CPU](#).

**Subtitle 4.11.4 GDMA Controller**

The GDMA Controller is a General Direct Memory Access (GDMA) controller that allows peripheral-to-memory, memory-to-peripheral, and memory-to-memory data transfer with the CPU’s intervention. The GDMA has six

[End of page]