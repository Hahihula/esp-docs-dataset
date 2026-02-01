**Title: Functional Description**

For details, see [ESP32-H2 Technical Reference Manual](#) > Chapter USB Serial/JTAG Controller (USB_SERIAL_JTAG).

---

### Pin Assignment

The pins USB_D+ and USB_D- for the USB Serial/JTAG Controller are multiplexed with GPIO26 ~ GPIO27 and FSPICS4 ~ FSPICS5 via IO MUX.

For more information about the pin assignment, see Section 2.3 IO Pins and [ESP32-H2 Technical Reference Manual](#) > Chapter IO MUX and GPIO Matrix.

---

#### Subtitle: 4.2.17 Two-wire Automotive Interface

The two-wire automotive interface (TWAI®) is a multi-master, multi-cast communication protocol designed for automotive applications. The TWAI controller facilitates the communication based on this protocol.

##### Feature List
- Compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- Standard frame format (11-bit ID) and extended frame format (29-bit ID)
- Bit rates from 1 Kbit/s to 1 Mbit/s
- Multiple modes of operation: Normal, Listen Only, and Self-Test (no acknowledgment required)
- Special transmissions: Single-shot and Self Reception
- Acceptance filter (single and dual filter modes)
- Error detection and handling: error counters, configurable error warning limit, error code capture, arbitration lost capture, automatic transceiver standby

For details, see [ESP32-H2 Technical Reference Manual](#) > Chapter Two-wire Automotive Interface.

---

### Pin Assignment
The pins for the two-wire automotive interface can be chosen from any GPIOs via the GPIO Matrix.
For more information about the pin assignment, see Section 2.3 IO Pins and [ESP32-H2 Technical Reference Manual](#) > Chapter IO MUX and GPIO Matrix.

---

#### Subtitle: 4.2.18 LED PWM Controller

The LED PWM Controller (LEDC) is designed to generate PWM signals for LED control.

##### Feature List
- Six independent PWM generators
- Maximum PWM duty cycle resolution of 20 bits
- Four independent timers with 20-bit counters, configurable fractional clock dividers and counter overflow values
- Adjustable phase of PWM signal output

---

**Footer:**
Espressif Systems  
Page number: 44  
[Submit Documentation Feedback](#)  
ESP32-H2 Series Datasheet v1.2