Title: Functional Description

Subtitle: Feature List

- **SPI Memory mode**
  In SPI memory mode, SPI0 and SPI1 interfaces are for external SPI memory. Data are transferred in unit of byte. Up to four-line STR reads and writes are supported. The clock frequency is configurable to a maximum of 120 MHz.

- **SPI2 General-purpose SPI (GP-SPI) mode**
  SPI2 can operate in master and slave modes. SPI2 supports two-line full-duplex communication and single/two/four-line half-duplex communication in both master and slave modes. The host’s clock frequency is configurable. Data are transferred in unit of byte. The clock polarity (CPOL) and phase (CPHA) are also configurable.
  - In master mode, the clock frequency is 80 MHz at most, and the four modes of SPI transfer format are supported.

- **In slave mode**
  The clock frequency is 40 MHz at most, and the four modes of SPI transfer format are also supported. 

For details, see [ESP32-C5 Technical Reference Manual > Chapter SPI Controller (SPI)](#).

Subtitle: Pin Assignment

For SPIO/1, the pins are multiplexed with GPIO15 ~ GPIO18 and GPIO20 ~ GPIO22 via the IO MUX.

For SPI2, the pins for data and clock signals are multiplexed with GPIO2 and GPIO4 ~ GPIO7 via the IO MUX. The pins for chip select signals for multiplexed with GPIO10 via the IO MUX. SPI2 signals can also be routed to any GPIOs via the GPIO matrix.

For more information about the pin assignment, see Section 2.3 IO Pins in [ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#).

Subtitle: I2C Controller

**4.2.1.3**

ESP32-C5 has an I2C and an LP I2C bus interface. I2C is used for I2C master mode or slave mode, depending on your configuration, while LP I2C is always in master mode.

Feature List
- standard mode (100 Kbit/s)
- fast mode (400 Kbit/s)
- up to 800 Kbit/s (constrained by SCL and SDA pull-up strength)
- 7-bit and 10-bit addressing mode
- double addressing mode
- 7-bit broadcast address

For details, see [ESP32-C5 Technical Reference Manual > Chapter I2C Controller (I2C)](#).

Footer: Espressif Systems  
Page number: 51  
Link: Submit Documentation Feedback