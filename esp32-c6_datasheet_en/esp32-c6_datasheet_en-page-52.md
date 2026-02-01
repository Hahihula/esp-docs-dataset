**4 Functional Description**

- Programmable digital noise filtering

- Support for 7-bit and 10-bit addressing, as well as dual address mode

For details, see [ESP32-C6 Technical Reference Manual > Chapter I2C Controller (I2C)](#).

---

### Pin Assignment

For details, see Section **2.3.5 Peripheral Pin Assignment**.

---

#### 4.2.1.4 I2S Controller

The I2S Controller in the ESP32-C6 chip provides a flexible communication interface for streaming digital data in multimedia applications, particularly digital audio applications.

##### Feature List
- Master mode and slave mode
- Full-duplex and half-duplex communications
- Separate TX and RX units that can work independently or simultaneously.
- A variety of audio standards supported:
  - TDM Philips standard
  - TDM MSB alignment standard
  - TDM PCM standard
  - PDM standard

##### Additional Features
- PCM-to-PDM TX interface
- Configurable high-precision BCK clock, with frequency up to 40 MHz (Sampling frequencies can be 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz, etc.)
- 8-/16-/24-/32-bit data communication
- Direct Memory Access (DMA)
- A-law and μ-law compression/decompression algorithms for improved signal-to-quantization noise ratio.
- Flexible data format control

For details, see [ESP32-C6 Technical Reference Manual > Chapter I2S Controller (I2S)](#).

---

### Pin Assignment

For details, see Section **2.3.5 Peripheral Pin Assignment**.

---

#### 4.2.1.5 Pulse Count Controller

The Pulse Count Controller (PCNT) is designed to count input pulses by tracking rising and falling edges of the input pulse signal.

Espressif Systems  
[Submit Documentation Feedback](#)

ESP32-C6 Series Datasheet v1.4