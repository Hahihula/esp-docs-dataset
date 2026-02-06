**Title: Peripherals**

- **7-bit broadcast address**
  For details, see [ESP32-C3 Technical Reference Manual > Chapter I2C Controller (I2C)](#).

---

**Pin Assignment**

For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).

---

### Subtitle: 5.2.1.4 I2S Controller

ESP8685 includes a standard I2S interface. This interface can operate as a master or a slave in full-duplex mode or half-duplex mode, and can be configured for 8-bit, 16-bit, 24-bit, or 32-bit serial communication. BCK clock frequency, from 10 kHz up to 40 MHz, is supported.

The I2S interface connects to the GDMA controller. The interface supports TDM PCM, TDM MSB alignment, TDM standard, and PDM standard.
For details, see [ESP32-C3 Technical Reference Manual > Chapter I2S Controller (I2S)](#).

---

**Pin Assignment**

For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).

---

### Subtitle: 5.2.1.5 USB Serial/JTAG Controller

ESP8685 integrates a USB Serial/JTAG controller. This controller has the following features:

- CDC-ACM virtual serial port and JTAG adapter functionality
- USB 2.0 full speed compliant, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- programming in-package flash
- CPU debugging with compact, JTAG instructions
- a full-speed USB PHY integrated in the chip

For details, see [ESP32-C3 Technical Reference Manual > Chapter USB Serial/JTAG Controller (USB_SERIAL_JTAG)](#).

---

**Pin Assignment**

For details, see [ESP8685 Series Datasheet > Section Peripheral Pin Assignment](#).

---

### Subtitle: 5.2.1.6 Two-wire Automotive Interface

ESP8685 has a TWAI® controller with the following features:

- compatible with ISO 11898-1 protocol (CAN Specification 2.0)
- standard frame format (11-bit ID) and extended frame format (29-bit ID)
- bit rates from 1 Kbit/s to 1 Mbit/s
- multiple modes of operation: Normal, Listen Only, and Self-Test (no acknowledgment required)

---

**Footer**

Espressif Systems  
Page number: 18  
Document version: ESP8685-WROOM-01 Datasheet v1.5

[Submit Documentation Feedback](#)