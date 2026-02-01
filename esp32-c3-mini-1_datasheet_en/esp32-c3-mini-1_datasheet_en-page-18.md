**Title: Peripherals**

- standard mode (100 Kbit/s)
- fast mode (400 Kbit/s)
- up to 800 Kbit/s (constrained by SCL and SDA pull-up strength)
- 7-bit and 10-bit addressing mode
- double addressing mode
- 7-bit broadcast address

For details, see [ESP32-C3 Technical Reference Manual > Chapter I2C Controller (I2C)](#).

---

**Title: Pin Assignment**

The pins for I2C can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-C3 Series Datasheet > Section IO Pins and ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

**Subtitle: 5.2.1.4 I2S Controller**

ESP32-C3 includes a standard I2S interface. This interface can operate as a master or a slave in full-duplex mode or half-duplex mode, and can be configured for 8-bit, 16-bit, 24-bit, or 32-bit serial communication. BCK clock frequency, from 10 kHz up to 40 MHz, is supported.

The I2S interface connects to the GDMA controller. The interface supports TDM PCM, TDM MSB alignment, TDM standard, and PDM standard.

For details, see [ESP32-C3 Technical Reference Manual > Chapter I2S Controller (I2S)](#).

---

**Subtitle: Pin Assignment**

The pins for the I2S Controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-C3 Series Datasheet > Section IO Pins and ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix](#).

---

**Subtitle: 5.2.1.5 USB Serial/JTAG Controller**

ESP32-C3 integrates a USB Serial/JTAG controller. This controller has the following features:

- CDC-ACM virtual serial port and JTAG adapter functionality
- USB 2.0 full speed compliant, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- programming in-package/off-package flash
- CPU debugging with compact JTAG instructions
- a full-speed USB PHY integrated in the chip

For details, see [ESP32-C3 Technical Reference Manual > Chapter USB Serial/JTAG Controller (USB_SERIAL_JTAG)](#).

---

**Footer:**
Espressif Systems  
18  
[Submit Documentation Feedback](#)  
ESP32-C3-MINI-1 & MINI-1U Datasheet v2.1