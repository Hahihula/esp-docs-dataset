**4 Functional Description**

- SCL clock stretching in slave mode
- Programmable digital noise filtering
- Support for 7-bit and 10-bit addressing, as well as dual address mode

**Pin Assignment**
For regular I2C, the pins used can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see Section **2.3 IO Pins**.

---

**4.2.1.4 I2S Controller**

The I2S Controller in the ESP32-C61 chip provides a flexible communication interface for streaming digital data in multimedia applications, particularly digital audio applications.

**Feature List**
- Master mode and slave mode
- Full-duplex and half-duplex communications
- Separate TX and RX units that can work independently or simultaneously

A variety of audio standards supported:
  - TDM Philips standard
  - TDM MSB alignment standard
  - TDM PCM standard
  - PDM standard

**PCM-to-PDM TX interface**

Configurable high-precision BCLK clock, with frequency up to 40 MHz.
- Sampling frequencies can be 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz,
  - etc.

**8-16/7-24/732-bit data communication**

Direct Memory Access (DMA)

A-law and μ-law compression/decompression algorithms for improved signal-to-quantization noise ratio

Flexible data format control

**Pin Assignment**
The pins for the I2S Controller can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see Section **2.3 IO Pins**.

---

Espressif Systems
46 ESP32-C61 Series Datasheet v0.5