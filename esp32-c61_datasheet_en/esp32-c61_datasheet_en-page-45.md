**Title: Functional Description**

---

### Features of SPI0 and SPI1

- Supports Single SPI, Dual SPI, Quad SPI, QPI modes
- Data transmission is in bytes

### Features of SPI2

- Supports operation as a master or slave
- Support for DMA
- Supports Single SPI, Dual SPI, Quad SPI, QPI modes
- Configurable clock polarity (CPOL) and phase (CPHA)
- Configurable clock frequency
- Data transmission is in bytes
- Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

#### As a master
- Supports 2-line full-duplex communication with clock frequency up to 80 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
- Provides six FSPICS... pins for connection with six independent SPI slaves

#### As a slave
- Supports 2-line full-duplex communication with clock frequency up to 60 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 60 MHz

---

### Pin Assignment

For SPI0/1, the pins are multiplexed with GPIO14 ~ GPIO17 and GPIO19 ~ GPIO20 via the IO MUX.

For SPI2, the pins for data and clock signals are multiplexed with GPIO2, GPIO7, and ITAG interface via the IO MUX. The pins for chip select signals for multiplexed with GPIO8 via the IO MUX.
For more information about the pin assignment, see Section 2.3 IO Pins.

---

### Subsection: 4.2.1.3 I2C Controller

The I2C Controller supports communication between the master and slave devices using the I2C bus.

#### Feature List
- Communication with multiple external devices
- Master and slave modes for I2C
- Standard mode (100 Kbit/s) and fast mode (400 Kbit/s)

---

**Footer:**
Espressif Systems  
Page 45 ESP32-C61 Series Datasheet v0.5