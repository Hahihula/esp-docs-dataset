**Title: Functional Description**

---

### **4.8.5 I2S Interface**

The I2S Controller in the ESP32 chip provides a flexible communication interface for streaming digital data in multimedia applications, particularly digital audio applications.

#### Feature List

- Master mode and slave mode
- Full-duplex and half-duplex communications
- A variety of audio standards supported
- Configurable high-precision output clock
- Supports PDM signal input and output
- Configurable data transmit and receive modes

For details, see [ESP32 Technical Reference Manual > Chapter I2S Controller](#).

---

### **4.8.6 Remote Control Peripheral**

The Remote Control Peripheral (RMT) controls the transmission and reception of infrared remote control signals.

#### Feature List

- Eight channels for sending and receiving infrared remote control signals
- Independent transmission and reception capabilities for each channel
- Clock divider counter, state machine, and receiver for each RX channel
- Supports various infrared protocols

For details, see [ESP32 Technical Reference Manual > Chapter Remote Control Peripheral](#).

#### Pin Assignment

The pins for the Remote Control Peripheral can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 4.10 Peripherals in Configurations and ESP32 Technical Reference Manual > Chapter IO_MUX and GPIO Matrix.

---

### **4.8.7 Pulse Counter Controller (PCNT)**

The pulse counter controller (PCNT) is designed to count input pulses by tracking rising and falling edges of the input pulse signal.

Espressif Systems  
[Submit Documentation Feedback](#)  
ESP32 Series Datasheet v5.2