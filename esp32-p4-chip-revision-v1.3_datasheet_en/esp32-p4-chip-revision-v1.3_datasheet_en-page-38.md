**Title: Functional Description**

- **Delta address mode and full address mode**
- A filter unit

- Notifying an instruction address via debug trigger or filter unit

- Support for the following sideband signals to control trace data flow:
  - Debugging trigger to start or end encoder
    - When the hart is halted, the encoder can report the last packet and then stop.
    - When the hart is reset, the encoder can report the last packet and then stop.

  - Stalling the hart when FIFO is almost full

- Arbitrary address range of the trace memory size

- Configurable synchronization modes:
  - Synchronization counter counts by packet
  - Synchronization counter counts by cycle
  - Synchronization counter can be disabled

- Trace lost status to indicate packet loss

- Automatic restart after packet loss

- Memory writing in the loop or non-loop mode

- Two interrupts:
  - Triggered when the packet size exceeds the configured memory space.
  - Triggered when a packet is lost.

- FIFO (128 x 8 bits) to buffer packets
- AHB burst transmission with configurable burst length

**Subtitle: Processor Instruction Extensions**

The ESP32-P4 HP 32-bit RISC-V dual-core processor supports standard RV32IMAFCZc extensions, and it also contains a custom extended instruction set Xhwl which reduces the number of instructions in the loop body to improve performance, and a custom AI and DSP extension Xai to improve operation efficiency of specific AI and DSP algorithms.

**Feature List**
- Eight new 128-bit general-purpose registers
- 128-bit vector operations, including complex multiplication, addition, subtraction, multiplication, shifting, and comparison.
- Combined data handling instructions and load/store operation instructions
- Aligned and unaligned 128-bit vector data load/store
- Configurable rounding and saturation modes

**Footer:**
Espressif Systems  
38  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback]