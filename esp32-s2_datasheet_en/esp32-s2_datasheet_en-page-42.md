**Title: Functional Description**

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter UART Controller (UART)](#).

## Pin Assignment

For details, see Section 2.3.6 Peripheral Pin Assignment.

### **4.2.1.5 I2C Controller**

ESP32-S2 has two I2C bus interfaces which can serve as I2C master or slave, depending on the user's configuration. The I2C interfaces support:

- standard mode (100 Kbit/s)
- fast mode (400 Kbit/s)
- up to 5 MHz (constrained by SDA pull-up strength)
- 7-bit/10-bit addressing mode
- dual addressing mode

Users can program command registers to control I2C interfaces, so that they have more flexibility.

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter I2C Controller (I2C)](#).

### **4.2.1.6 I2S Controller**

ESP32-S2 includes a standard I2S interface. It can operate in master or slave mode, in full-duplex and half-duplex communication modes, and can be configured to operate with an 8-/16-/24-/32-bit resolution as an input or output channel. BCK clock frequency, from 10 kHz up to 40 MHz, is supported.

The I2S interface has a dedicated DMA controller. PCM interface is supported.

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter I2S Controller (I2S)](#).

### **4.2.1.7 Camera Interface**

ESP32-S2 supports one 8 or 16-bit DVP image sensor, with clock frequency of up to 40 MHz. The camera interface is implemented by using the hardware resources of I2S.

For more information, please refer to [ESP32-S2 Technical Reference Manual > Chapter I2S Controller (I2S)](#).

---

**Footer:**
Espressif Systems
Page number: 42
Document version: ESP32-S2 Series Datasheet v1.8

[Submit Documentation Feedback](#)