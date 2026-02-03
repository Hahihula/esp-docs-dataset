**Title: Peripherals**

---

### Pin Assignment

For SPI0/1, the pins are multiplexed with GPIO14 ~ GPIO17 and GPIO19 ~ GPIO20 via the IO MUX.

For SPI2, the pins for data and clock signals are multiplexed with GPIO2, GPIO7, and JTAG interface via the IO MUX. The pins for chip select signals for multiplexed with GPIO8 via the IO MUX.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet](#) > Section 10 Pins.

---

### **5.2.1.3 I2C Controller**

The I2C Controller supports communication between the master and slave devices using the I2C bus.

#### Feature List

- Communication with multiple external devices
- Master and slave modes for I2C
- Standard mode (100 Kbit/s) and fast mode (400 Kbit/s)
- SCL clock stretching in slave mode
- Programmable digital noise filtering
- Support for 7-bit and 10-bit addressing, as well as dual address mode

---

### Pin Assignment

For regular I2C, the pins used can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet](#) > Section 10 Pins.

---

### **5.2.1.4 I2S Controller**

The I2S Controller in the ESP32-C61 chip provides a flexible communication interface for streaming digital data in multimedia applications, particularly digital audio applications.

#### Feature List

- Master mode and slave mode
- Full-duplex and half-duplex communications
- Separate TX and RX units that can work independently or simultaneously
- A variety of audio standards supported:
  - TDM Philips standard
  - TDM MSB alignment standard
  - TDM PCM standard
  - PDM standard
- PCM-to-PDM TX interface
- Configurable high-precision BCK clock, with frequency up to 40 MHz

---

**Footer:**

Espressif Systems  
[Submit Documentation Feedback](#) ESP32-C61-MINI-1 & MINI-1U Datasheet v0.6