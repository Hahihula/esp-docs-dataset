**Title: Functional Description**

---

### Pin Assignment

For details, see Section **2.3.4 Peripheral Pin Assignment**.

#### 4.2.1.5 USB Serial/JTAG Controller

ESP32-C3 integrates a USB Serial/JTAG controller. This controller has the following features:

- CDC-ACM virtual serial port and JTAG adapter functionality
- USB 2.0 full speed compliant, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- programming in-package/off-package flash
- CPU debugging with compact JTAG instructions
- a full-speed USB PHY integrated in the chip

For details, see **ESP32-C3 Technical Reference Manual** > Chapter USB Serial/JTAG Controller (USB_SERIAL_JTAG).

---

### Pin Assignment

For details, see Section 2.3.4 Peripheral Pin Assignment.

#### 4.2.1.6 Two-wire Automotive Interface

ESP32-C3 has a TWAI® controller with the following features:

- compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- standard frame format (11-bit ID) and extended frame format (29-bit ID)
- bit rates from 1 Kbit/s to 1 Mbit/s
- multiple modes of operation: Normal, Listen Only, and Self-Test (no acknowledgment required)
- 64-byte receive FIFO
- acceptance filter (single and dual filter modes)
- error detection and handling: error counters, configurable error interrupt threshold, error code capture, arbitration lost capture

For details, see **ESP32-C3 Technical Reference Manual** > Chapter Two-wire Automotive Interface.

---

### Pin Assignment

For details, see Section 2.3.4 Peripheral Pin Assignment.

#### 4.2.1.7 LED PWM Controller

The LED PWM controller can generate independent digital waveform on six channels. The LED PWM controller:

[End of visible text]