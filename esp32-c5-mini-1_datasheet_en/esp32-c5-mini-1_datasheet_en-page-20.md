**Title: Peripherals**

---

### Section Title

5.2.1.3 I2C Controller

ESP32-C5 has an I2C and an LP I2C bus interface. I2C is used for I2C master mode or slave mode, depending on your configuration, while LP I2C is always in master mode.

---

#### Feature List
- standard mode (100 Kbit/s)
- fast mode (400 Kbit/s)
- up to 800 Kbit/s (constrained by SCL and SDA pull-up strength)
- 7-bit and 10-bit addressing mode
- double addressing mode
- 7-bit broadcast address

For details, see [ESP32-C5 Technical Reference Manual > Chapter I2C Controller (I2C)](#).

---

#### Pin Assignment
For regular I2C, the pins used can be chosen from any GPIOs via the GPIO Matrix.
For LP I2C, the pins used are multiplexed with LP_GPIO2 and LP_GPIO3 via LP IO MUX.

For more information about the pin assignment, see [ESP32-C5 Series Datasheet > Section 10 Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#).

---

### Subsection Title

5.2.1.4 I2S Controller

ESP32-C5 includes a standard I2S interface. This interface can operate as a master or a slave in full-duplex mode or half-duplex mode, and supports 8-bit, 16-bit, 24-bit, or 32-bit serial communication. BCK clock frequency, from 10 kHz up to 40 MHz, is supported.

The I2S interface supports TDM Philips, TDM MSB alignment, TDM PCM standard, PDM standard, and PCM-to-PDM TX interface. It connects to the GDMA controller.

---

#### Feature List
- master mode and slave mode
- full-duplex and half-duplex communications
- separate TX and RX units that can work independently or simultaneously

a variety of audio standards supported:
  - TDM Philips standard
  - TDM MSB alignment standard
  - TDM PCM standard
  - PDM standard
  - various TX/RX modes

---

**Footer**

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C5-MINI-1 Datasheet v1.0