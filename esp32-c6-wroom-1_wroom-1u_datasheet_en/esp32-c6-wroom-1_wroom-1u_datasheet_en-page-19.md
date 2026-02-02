**Title: Peripherals**

- **Subtitle:** Pin Assignment

For details, see [ESP32-C6 Series Datasheet](#) > Section Peripheral Pin Assignment.

---

**5.2.1.3 I2C Controller**

The I2C Controller supports communication between the master and slave devices using the I2C bus.

**Feature List**
- Two I2C controllers: one in the main system and one in the low-power system
- Communication with multiple external devices
- Master and slave modes for I2C, and master mode only for LP I2C
- Standard mode (100 Kbit/s) and fast mode (400 Kbit/s)
- SCL clock stretching in slave mode
- Programmable digital noise filtering
- Support for 7-bit and 10-bit addressing, as well as dual address mode

---

**5.2.1.4 I2S Controller**

The I2S Controller in the ESP32-C6 chip provides a flexible communication interface for streaming digital data in multimedia applications, particularly digital audio applications.

**Feature List**
- Master mode and slave mode
- Full-duplex and half-duplex communications
- Separate TX and RX units that can work independently or simultaneously.
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
[Submit Documentation Feedback](#)  
ESP32-C6-WROOM-1 & WROOM-1U Datasheet v1.4