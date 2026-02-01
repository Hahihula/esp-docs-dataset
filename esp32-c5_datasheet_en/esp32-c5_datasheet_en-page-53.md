**Title: Functional Description**

- **Subsection:** direct memory access

- **Subsection:** standard I2S interface interrupts

For details, see [ESP32-C5 Technical Reference Manual > Chapter 12S Controller (I2S)](#).

---

**Pin Assignment**

The pins for the I2S controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section **2.3 IO Pins** and [ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#).

---

**4.2.1.5 USB Serial/JTAG Controller**

ESP32-C5 contains a USB Serial/JTAG controller. This unit can be used to program the SoC's flash, read program output, as well as attach a debugger to the running program. All of these are possible for any computer with a USB host without any active external components.

**Feature List**
- USB 2.0 full speed compliant, capable of up to 12 Mbit/s transfer speed (note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality
- programming the chip's flash
- CPU debugging with compact JTAG instructions
- a full-speed USB PHY integrated in the chip

For details, see [ESP32-C5 Technical Reference Manual > Chapter USB Serial/JTAG Controller (USB_SERIAL_JTAG)](#).

---

**Pin Assignment**

The pins for the USB Serial/JTAG controller are multiplexed with GPIO13 ~ GPIO14 via IO MUX. GPIO13 ~ GPIO14 are also multiplexed with the pins for the SDIO Slave controller. The SDIO Slave controller can be used together with the USB Serial/JTAG controller in single SPI mode, but not in quad SPI mode.

For more information about the pin assignment, see Section **2.3 IO Pins** and [ESP32-C5 Technical Reference Manual > Chapter GPIO Matrix and IO MUX](#).

---

**4.2.1.6 CAN FD Controller**

The Controller Area Network Flexible Data-Rate (CAN FD) is a multi-master, multi-cast communication protocol designed for automotive applications. The CAN FD controller facilitates the communication based on this protocol.

**Feature List**
- compliant with ISO11898-1:2015
- RX buffer FIFO with 32 - 4096 words (1 - 204 CAN FD frames with 64 byte of data)

Espressif Systems

[Submit Documentation Feedback](#)