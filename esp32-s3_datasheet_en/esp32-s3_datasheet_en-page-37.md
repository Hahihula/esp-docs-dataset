**Title: Functional Description**

- **Saturation operation**
  
For details, see [ESP32-S3 Technical Reference Manual > Chapter Processor Instruction Extensions](#).

---

### Section 4.1.1.3 Ultra-Low-Power Coprocessor (ULP)

The ULP coprocessor is designed as a simplified, low-power replacement of CPU in sleep modes. It can be also used to supplement the functions of the CPU in normal working mode. The ULP coprocessor and RTC memory remain powered up during the Deep-sleep mode. Hence, the developer can store a program for the ULP coprocessor in the RTC slow memory to access RTC GPIO, RTC peripheral devices, RTC timers and internal sensors in Deep-sleep mode.

ESP32-S3 has two ULP coprocessors, one based on RISC-V instruction set architecture (ULP-RISC-V) and the other on finite state machine (ULP-FSM). The clock of the coprocessors is the internal fast RC oscillator.

#### Feature List

- **ULP-RISC-V:**
  - Support for [RV32IMC](#) instruction set
  - Thirty-two 32-bit general-purpose registers
  - 32-bit multiplier and divider
  - Support for interrupts
  - Booted by the CPU, its dedicated timer, or RTC GPIO

- **ULP-FSM:**
  - Support for common instructions including arithmetic, jump, and program control instructions
  - Support for on-board sensor measurement instructions
  - Booted by the CPU, its dedicated timer, or RTC GPIO

**Note:** Note that these two coprocessors cannot work simultaneously.

For details, see [ESP32-S3 Technical Reference Manual > Chapter ULP Coprocessor](#).

---

### Section 4.1.1.4 GDMA Controller (GDMA)

ESP32-S3 has a general-purpose DMA controller (GDMA) with five independent channels for transmitting and another five independent channels for receiving. These ten channels are shared by peripherals that have DMA feature, and support dynamic priority.

The GDMA controller controls data transfer using linked lists. It allows peripheral-to-memory and memory-to-memory data transfer at a high speed. All channels can access internal and external RAM.

The ten peripherals on ESP32-S3 with DMA feature are SPI2, SPI3, UHCI0, I2S0, I2S1, LCD/CAM, AES, SHA, ADC, and RMT.

For details, see [ESP32-S3 Technical Reference Manual > Chapter GDMA Controller](#).

---

**Footer:**
Espressif Systems
Page 37 of ESP32-S3 Series Datasheet v2.1

[Submit Documentation Feedback](#)