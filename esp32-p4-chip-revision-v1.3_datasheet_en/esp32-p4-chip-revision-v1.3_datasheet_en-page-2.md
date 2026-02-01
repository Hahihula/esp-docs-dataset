Title: Product Overview

Body Text:
ESP32-P4 is a high-performance MCU that supports large internal memory and has powerful image and voice processing capabilities. The MCU consists of a High Performance (HP) system and a Low Power (LP) system. The HP system contains a RISC-V dual-core CPU and rich peripherals, while the LP system contains a low-power RISC-V single-core CPU and various peripherals optimized for low-power applications.

The functional block diagram of the SoC is shown below:

Functional Block Diagram:
- ESP32-P4 — Espressif's High Performance MCU

HP Core System
- HPSPM (High Performance System)
  - RISC-V 32-bit Dual-core Microprocessor, L2MEM Cache at 360 MHz
- LP Core System
  - RISC-V 32-bit Single-core Microprocessor @40 MHz with LPROM and JTAG
- Low Power System
  - Power Management Unit (PMU), BAT Power Supply

LP Peripherals:
- LP SPI, LP I2C, LP I2S, LP Mailbox,
- LP UART, LP GPIO,
- LP DIG ADC, Temperature Sensor,

Touch Sensor, eFuse Controller.

HP Peripherals include various modules such as:
- SPI
- I2C with PDM (Pulse Density Modulation)
- I2S with PDM
- DIG ADC Controller
- ISP
- PPA

And many more...

Security includes features like:
- RSA ECC,
- SHA, HMAC,

and others.

Modules having power in specific modes are indicated by color-coded blocks. The diagram shows the distribution of modules across different sleep states (Active Light-sleep) and optional deep-sleep mode options for certain functions such as I2C Master & Slave or MIPI CSI.

Footer:
ESP32-P4 Functional Block Diagram

Note: There is a sidebar on the left side with text "Submit Documentation Feedback" followed by an arrow pointing to page 2, indicating that this document has multiple pages. The bottom of the image shows part of another title which seems incomplete and reads "...SP32-P4 Series Datasheet v0.6".