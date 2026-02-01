**Title: Functional Description**

---

### Features of SPI0 and SPI1

- Supports Single SPI, Dual SPI, Quad SPI (QPI) modes
- Data transmission is in bytes

### Features of SPI2

- Supports operation as a master or slave
  - Support for GDMA
  - Supports Single SPI, Dual SPI, Quad SPI (QPI) modes
    - Configurable clock polarity (CPOL) and phase (CPHA)
    - Configurable clock frequency
      - Data transmission is in bytes
        - Configurable read and write data bit order: most-significant bit (MSB) first, or least-significant bit (LSB) first

#### As a master
- Supports 2-line full-duplex communication with clock frequency up to 80 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
- Provides six FSPICS... pins for connection with six independent SPI slaves

#### As a slave
- Supports 2-line full-duplex communication with clock frequency up to 40 MHz
- Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 40 MHz

For details, see [ESP32-C6 Technical Reference Manual](#) > Chapter SPI Controller (SPI).

---

### Pin Assignment

For details, see Section **2.3.5 Peripheral Pin Assignment**.

---

#### I2C Controller
The I2C Controller supports communication between the master and slave devices using the I2C bus.

##### Feature List
- Two I2C controllers: one in the main system and one in the low-power system
- Communication with multiple external devices
- Master and slave modes for I2C, and master mode only for LP I2C
- Standard mode (100 Kbit/s) and fast mode (400 Kbit/s)
- SCL clock stretching in slave mode

---

**Footer:**
Espressif Systems  
Page 51 of ESP32-C6 Series Datasheet v1.4  

[Submit Documentation Feedback](#)