**Title: Peripherals**

---

### Pin Assignment

The pins for the USB Serial/JTAG Controller are multiplexed with GPIO18 ~ GPIO19.

For more information about the pin assignment, see [ESP32-C3 Series Datasheet](#) > Section 10 Pins and ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

---

#### **5.2.1.6 Two-wire Automotive Interface**

ESP32-C3 has a TWAI® controller with the following features:

- compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- standard frame format (11-bit ID) and extended frame format (29-bit ID)
- bit rates from 1 Kbit/s to 1 Mbit/s
- multiple modes of operation: Normal, Listen Only, and Self-Test (no acknowledgment required)
- 64-byte receive FIFO
- acceptance filter (single and dual filter modes)
- error detection and handling: error counters, configurable error interrupt threshold, error code capture, arbitration lost capture

For details, see [ESP32-C3 Technical Reference Manual](#) > Chapter Two-wire Automotive Interface.

---

#### **5.2.1.7 LED PWM Controller**

The LED PWM controller can generate independent digital waveform on six channels. The LED PWM controller:

- Can generate digital waveform with configurable periods and duty cycle, the resolution of duty cycle can be up to 14 bits.
- Has multiple clock sources, including APB clock and external main crystal clock.
- Can operate when the CPU is in Light-sleep mode.
- Supports gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator.

For details, see [ESP32-C3 Technical Reference Manual](#) > Chapter LED PWM Controller.

---

### Pin Assignment

The pins for the Two-wire Automotive Interface can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see [ESP32-C3 Series Datasheet](#) > Section 10 Pins and ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

---

### Pin Assignment

The pins for the LED PWM Controller can be chosen from any GPIOs via the GPIO Matrix. For more information about the pin assignment, see [ESP32-C3 Series Datasheet](#) > Section 10 Pins and ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

---

**Footer:**
Espressif Systems
Page number: 19

Submit Documentation Feedback