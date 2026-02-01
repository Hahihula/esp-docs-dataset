**Title: Functional Description**

---

### Feature List

- Standard mode (100 kbit/s)
- Fast mode (400 kbit/s)
- Up to 800 kbit/s (constrained by SCL and SDA pull-up strength)
- 7-bit and 10-bit addressing mode
- Double addressing mode (slave addressing and slave register addressing)

The hardware provides a command abstraction layer to simplify the usage of the I2C peripheral.

For details, see [ESP32-S3 Technical Reference Manual > Chapter I2C Controller](#).

---

### Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

#### 4.2.1.3 I2S Interface

ESP32-S3 includes two standard I2S interfaces. They can operate in master mode or slave mode, in full-duplex mode or half-duplex communication mode, and can be configured to operate with an 8-bit, 16-bit, 24-bit, or 32-bit resolution as an input or output channel. BCK clock frequency, from 10 kHz up to 40 MHz, is supported.

The I2S interface has a dedicated DMA controller. It supports TDM PCM, TDM MSB alignment, TDM LSB alignment, TDM Phillips, and PDM interface.

For details, see [ESP32-S3 Technical Reference Manual > Chapter I2S Controller](#).

---

#### Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

#### 4.2.1.4 LCD and Camera Controller

The LCD and Camera controller of ESP32-S3 consists of a LCD module and a camera module.

The LCD module is designed to send parallel video data signals, and its bus supports 8-bit ~ 16-bit parallel RGB, I8080, and MOTO6800 interfaces. These interfaces operate at 40 MHz or lower, and support conversion among RGB565, YUV422, YUV420, and YUV411.

The camera module is designed to receive parallel video data signals, and its bus supports an 8-bit ~ 16-bit DVP image sensor, with clock frequency of up to 40 MHz. The camera interface supports conversion among RGB565, YUV422, YUV420, and YUV411.

For details, see [ESP32-S3 Technical Reference Manual > Chapter LCD and Camera Controller](#).

---

#### Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

**Footer:**
Espressif Systems  
Page number: 52  
Document title: ESP32-S3 Series Datasheet v2.1