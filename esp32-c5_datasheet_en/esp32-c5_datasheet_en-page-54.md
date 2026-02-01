**Title: Functional Description**

- **2 - 8 TXT buffers (1 CAN FD frame in each TXT buffer)**
- **32-bit slave memory interface (APB, AHB, RAM-like interface)**
- **support of ISO and non-ISO CAN FD protocol**
- **timestamping and time triggered transmission**
- **support interrupts**

- **loopback mode, bus monitoring mode, ACK forbidden mode, self-test mode, and restricted operation mode**

**For details, see ESP32-C5 Technical Reference Manual > Chapter Controller Area Network Flexible Data-Rate.**

---

**Subtitle: Pin Assignment**

The pins for the CAN FD Controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

**Title: LED PWM Controller (4.2.1.7)**

The LED PWM controller can generate independent digital waveform on six channels.

**Subtitle: Feature List**

- generating digital waveform with configurable periods and duty cycle. The resolution of duty cycle can be up to 20 bits
- multiple clock sources, including 80 MHz PLL clock, external main crystal clock, and internal fast RC oscillator
- operation when the CPU is in Light-sleep mode
- gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator
- up to 16 duty cycle ranges for gamma curve generation, each can be independently configured in terms of duty cycle direction (increase or decrease), step size, the number of steps, and step frequency

For details, see ESP32-C5 Technical Reference Manual > Chapter LED PWM Controller.

**Subtitle: Pin Assignment**

The pins for the LED PWM controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX.

---

**Title: Pulse Count Controller (4.2.1.8)**

The Pulse Count controller (PCNT) in ESP32-C5 captures pulses and counts pulse edges in seven modes.

Espressif Systems  
Submit Documentation Feedback  
ESP32-C5 Series Datasheet v1.0