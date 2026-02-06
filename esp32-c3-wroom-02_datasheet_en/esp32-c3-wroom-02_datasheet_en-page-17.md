**Title: Peripherals**

- **SPI2**: is a general purpose SPI controller with access to a DMA channel allocated by the GDMA controller

**Subtitle: Features of SPI0 and SPI1**
- Supports Single SPI, Dual SPI, and Quad SPI, QPI modes
- Configurable clock frequency with a maximum of 120 MHz in Single Transfer Rate (STR) mode
- Data transmission is in bytes

**Subtitle: Features of SPI2**
- Supports operation as a master or slave
- Connects to a DMA channel allocated by the GDMA controller
- Supports Single SPI, Dual SPI, and Quad SPI, QPI
- Configurable clock polarity (CPOL) and phase (CPHA)
- Configurable clock frequency
- Data transmission is in bytes
- Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

**As a master**
- Supports 2-line full-duplex communication with clock frequency up to 80 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
- Provides six SPI_CS pins for connection with six independent SPI slaves
- Configurable CS setup time and hold time

**As a slave**
- Supports 2-line full-duplex communication with clock frequency up to 60 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 60 MHz

For details, see [ESP32-C3 Technical Reference Manual > Chapter SPI Controller (SPI)](#).

**Subtitle: Pin Assignment**
For SPI0/1, the pins are multiplexed with GPIO12 ~ GPIO17 via the IO MUX.
For SPI2, the pins are multiplexed with GPIO2, GPIO4 ~ GPIO7, GPIO10, and JTAG interface via the IO MUX.

For more information about the pin assignment, see [ESP32-C3 Series Datasheet > Section 10 Pins and ESP32-C3 Technical Reference Manual > Chapter I/O MUX and GPIO Matrix](#).

**Subtitle: 5.2.1.3 I2C Controller**
ESP32-C3 has an I2C bus interface which is used for I2C master mode or slave mode, depending on your configuration. The I2C interface supports:

[Footer: Espressif Systems | Page number: 17 | Document version: ESP32-C3-WROOM-02 & WROOM-02U Datasheet v1.6]