**Title: Peripherals**

- **Bullet Point:** UART as the wake-up source

- **Subheading:** software and hardware flow control

For details, see [ESP32-C5 Technical Reference Manual > Chapter UART Controller (UART)](#).

---

**Subtitle: Pin Assignment**

The pins connected to transmit and receive signals (UOTXD and UORXD) for UART0 are multiplexed with GPIO11 and GPIO12 via IO MUX. Other signals can be routed to any GPIOs via the GPIO matrix.

For LP UART, the pins used are multiplexed with LP_GPIO0 ~ LP_GPIO5 via LP IO MUX.

For more information about the pin assignment, see [ESP32-C5 Series Datasheet > Section IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#).

---

**Subtitle: 5.2.1.2 SPI Controller**

ESP32-C5 features three SPI interfaces (SPI0, SPI1, and SPI2). SPI0 and SPI1 can be configured to operate in SPI memory mode, while SPI2 can be configured to operate in general-purpose SPI mode.

**Subheading:** Feature List

- **Bullet Point:** SPI Memory mode
  - In SPI memory mode, SPI0 and SPI1 interfaces are for external SPI memory. Data are transferred in unit of byte. Up to four-line STR reads and writes are supported. The clock frequency is configurable to a maximum of 120 MHz.

- **Bullet Point:** SPI2 General-purpose SPI (GP-SPI) mode
  - SPI2 can operate in master and slave modes. SPI2 supports two-line full-duplex communication and single/two/four-line half-duplex communication in both master and slave modes. The host’s clock frequency is configurable.
    - Data are transferred in unit of byte. The clock polarity (CPOL) and phase (CPHA) are also configurable.

  - In master mode, the clock frequency is 80 MHz at most, and the four modes of SPI transfer format are supported.

  - In slave mode, the clock frequency is 40 MHz at most, and the four modes of SPI transfer format are also supported.
  
For details, see [ESP32-C5 Technical Reference Manual > Chapter SPI Controller (SPI)](#).

---

**Subtitle: Pin Assignment**

For SPIO/1, the pins are multiplexed with GPIO15 ~ GPIO18 and GPIO20 ~ GPIO22 via the IO MUX.

For SPI2, the pins for data and clock signals are multiplexed with GPIO2 and GPIO4 ~ GPIO7 via the IO MUX. The pins for chip select signals for multiplexed with GPIO10 via the IO MUX. SPI2 signals can also be routed to any GPIOs via the GPIO matrix.

For more information about the pin assignment, see [ESP32-C5 Series Datasheet > Section IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#).

---

**Footer:**
Espressif Systems
Page 22 of ESP32-C5-WROOM-1 & WROOM-1U Datasheet v0.8 PRELIMINARY

[Submit Documentation Feedback]