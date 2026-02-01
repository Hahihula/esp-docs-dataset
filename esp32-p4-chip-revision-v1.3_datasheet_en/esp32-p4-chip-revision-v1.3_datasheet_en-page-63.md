**Title: Functional Description**

- **Subsection:** DMA-controlled single transfer or segmented transfer as slave; data length is unlimited

- **Subsection:** Configurable bit read/write order

- **Subsection:** Independent interrupts for CPU-controlled transfer and DMA-controlled transfer

- **Subsection:** Configurable clock polarity and phase

- **Subsection:** Four SPI clock modes: mode 0-mode 3

- **Subsection:** Multiple CS lines as master
  - GP-SPI2: CSO-CS5
  - GP-SPI3: CSO-CS2

- **Subsection:** Able to communicate with SPI devices, such as a sensor, a screen controller, as well as a flash or RAM chip

**Title: LP-SPI**

LP-SPI is a simplified version of GP-SPI and has a subset of GP-SPI’s features:

- Works as a master or as a slave
- Half- and full-duplex communications
- CPU-controlled transfer
- 1-bit SPI data mode
- Configurable module clock frequency:
  - Master: up to 40 MHz
  - Slave: up to 40 MHz

**Subsection:** Configurable data length:
  - CPU-controlled transfer as master or as slave: 1–64 bytes

**Subsection:** Configurable bit read/write order

**Subsection:** Interrupts for CPU-controlled transfer

**Subsection:** Configurable clock polarity and phase

**Subsection:** Four SPI clock modes: mode 0-mode 3
- One CS line as master: CSO
- Wake-up feature as slave (the only new feature compared with GP-SPI)

**Title: Pin Assignment**

The Flash SPI interface uses the dedicated digital pins 27–33.

The GP-SPI2 controller includes one four-line interface and one eight-line interface. The pins connected to the four-line interface are multiplexed with GPIO6-GPIO11 via the IO MUX. The pins connected to the eight-line interface are multiplexed with GPIO28-GPIO38, UART0 interface, and the first RMII interface of EMAC controller via the IO MUX. If high-speed performance is not critical for the GP-SPI2 interface, you can select pins from any GPIOs via the GPIO Matrix.

For GP-SPI3, the pins used can be chosen from any GPIOs via the GPIO Matrix.

**Footer:**
- Espresso Systems
- Submit Documentation Feedback

**Document Information:** 
ESP32-P4 Series Datasheet v0.6