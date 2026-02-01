**Title: Functional Description**

---

### Pin Assignment

For regular I2C, the pins used can be chosen from any GPIOs via the GPIO Matrix.

For LP I2C, the pins used are multiplexed with LP_GPIO2 and LP_GPIO3 via LP IO MUX.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

### **4.2.1.4 I2S Controller**

ESP32-C5 includes a standard I2S interface. This interface can operate as a master or a slave in full-duplex mode or half-duplex mode, and supports 8-bit, 16-bit, 24-bit, or 32-bit serial communication. BCK clock frequency, from 10 kHz up to 40 MHz, is supported.

The I2S interface supports TDM Philips, TDM MSB alignment, TDM PCM standard, PDM standard, and PCM-to-PDM TX interface. It connects to the GDMA controller.

---

#### Feature List

- master mode and slave mode
- full-duplex and half-duplex communications
- separate TX and RX units that can work independently or simultaneously
- a variety of audio standards supported:
  - TDM Philips standard
  - TDM MSB alignment standard
  - TDM PCM standard
  - PDM standard

#### Various TX/RX modes

- TDM TX mode, up to 16 channels supported
- TDM RX mode, up to 16 channels supported
- PDM TX mode: 
  - raw PDM data transmission
  - PCM-to-PDM data format conversion, up to 2 channels supported
- PDM RX mode:
  - raw PDM data reception

#### Additional Features:

- configurable clock source with frequency up to 240 MHz
- configurable high-precision sample clock with a variety of sampling frequencies supported
- 8/16/24/32-bit data width
- synchronous counter in TX mode
- ETM feature

---

**Footer:**

Espressif Systems  
52  
ESP32-C5 Series Datasheet v1.0  

[Submit Documentation Feedback](#)