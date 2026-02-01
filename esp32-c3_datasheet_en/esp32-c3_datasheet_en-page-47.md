**Title: Functional Description**

- **Configurable read and write data bit order:** most-significant bit (MSB) first, or least-significant bit (LSB)
  
  - As a master:
    - Supports 2-line full-duplex communication with clock frequency up to 80 MHz
    - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 80 MHz
    - Provides six SPI_CS pins for connection with six independent SPI slaves
    - Configurable CS setup time and hold time
  
  - As a slave:
    - Supports 2-line full-duplex communication with clock frequency up to 60 MHz
    - Supports 1-, 2-, 4-line half-duplex communication with clock frequency up to 60 MHz

For details, see ESP32-C3 Technical Reference Manual > Chapter SPI Controller (SPI).

---

**Title: Pin Assignment**

For details, see Section 2.3.4 Peripheral Pin Assignment.

---

**Subtitle: 4.2.1.3 I2C Controller**

ESP32-C3 has an I2C bus interface which is used for I2C master mode or slave mode, depending on your configuration. The I2C interface supports:

- standard mode (100 Kbit/s)
- fast mode (400 Kbit/s)
- up to 800 Kbit/s (constrained by SCL and SDA pull-up strength)
- 7-bit and 10-bit addressing mode
- double addressing mode
- 7-bit broadcast address

For details, see ESP32-C3 Technical Reference Manual > Chapter I2C Controller (I2C).

---

**Subtitle: Pin Assignment**

For details, see Section 2.3.4 Peripheral Pin Assignment.

---

**Subtitle: 4.2.1.4 I2S Controller**

ESP32-C3 includes a standard I2S interface. This interface can operate as a master or a slave in full-duplex mode or half-duplex mode, and can be configured for 8-bit, 16-bit, 24-bit, or 32-bit serial communication. BCK clock frequency, from 10 kHz up to 40 MHz, is supported.

The I2S interface connects to the GDMA controller. The interface supports TDM PCM, TDM MSB alignment, TDM standard, and PDM standard.

For details, see ESP32-C3 Technical Reference Manual > Chapter I2S Controller (I2S).

---

**Footer:**
Espressif Systems
47
ESP32-C3 Series Datasheet v2.2

Submit Documentation Feedback