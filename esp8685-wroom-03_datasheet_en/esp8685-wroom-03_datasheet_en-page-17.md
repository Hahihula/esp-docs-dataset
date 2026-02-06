**Title: Peripherals**

- Configurable clock frequency with a maximum of 120 MHz in Single Transfer Rate (STR) mode

- Data transmission is in bytes

---

### Features of SPI2

- Supports operation as a master or slave
- Connects to a DMA channel allocated by the GDMA controller
- Supports Single SPI, Dual SPI, and Quad SPI, QPI
- Configurable clock polarity (CPOL) and phase (CPHA)
- Configurable clock frequency
- Data transmission is in bytes
- Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

#### As a master
  - Supports 2-line full-duplex communication with clock frequency up to 80 MHz
  - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
  - Provides six SPI_CS pins for connection with six independent SPI slaves
  - Configurable CS setup time and hold time

#### As a slave
  - Supports 2-line full-duplex communication with clock frequency up to 60 MHz
  - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 60 MHz

---

### Pin Assignment

For details, see [ESP8685 Series Datasheet](#) > Section Peripheral Pin Assignment.

---

**Title: I2C Controller**

ESP8685 has an I2C bus interface which is used for I2C master mode or slave mode, depending on your configuration. The I2C interface supports:

- standard mode (100 Kbit/s)
- fast mode (400 Kbit/s)
- up to 800 Kbit/s (constrained by SCL and SDA pull-up strength)
- 7-bit and 10-bit addressing mode
- double addressing mode
- 7-bit broadcast address

---

**Footer:**
Espressif Systems  
[Submit Documentation Feedback](#) ESP8685-WROOM-03 Datasheet v1.5