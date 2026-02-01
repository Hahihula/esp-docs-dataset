**Title: Functional Description**

---

### Features of SPI2

- Supports operation as a master or slave
- Support for DMA
- Supports Single SPI, Dual SPI, Quad SPI, QPI modes
- Configurable clock polarity (CPOL) and phase (CPHA)
- Configurable clock frequency
- Data transmission is in bytes
- Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

#### As a master
- Supports 2-line full-duplex communication with clock frequency up to 48 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 48 MHz
- Provides six FSPICS... pins for connection with six independent SPI slaves
- Configurable CS setup time and hold time

#### As a slave
- Supports 2-line full-duplex communication with clock frequency up to 32 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 32 MHz

For details, see [ESP32-H2 Technical Reference Manual > Chapter SPI Controller (SPI)](#).

---

### Pin Assignment

#### Via IO MUX
For SPI2, the pins for data and clock signals are multiplexed with GPIO0, GPIO2 ~ GPIO5, and JTAG interface via the IO MUX. The pins for chip select signals are multiplexed with GPIO1, GPIO23 ~ GPIO27, UART0 interface, and USB interface via the IO MUX.

#### Via GPIO Matrix
The pins for SPI2 can be chosen from any GPIOs via the GPIO matrix.
For more information about the pin assignment, see Section 2.3 IO Pins and [ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

### 4.2.1.3 I2C Controller

The I2C Controller supports communication between the master and slave devices using the I2C bus.

#### Feature List
- Two I2C controllers
- Communication with multiple external devices
- Master and slave modes

---

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-H2 Series Datasheet v1.2