**Title: Peripherals**

- **TDM TX mode**, up to 16 channels supported
- TDM RX mode, up to 16 channels supported
- PDM TX mode

    * raw PDM data transmission
    * PCM-to-PDM data format conversion, up to 2 channels supported

- PDM RX mode

    * raw PDM data reception

**Features:**

- configurable clock source with frequency up to 240 MHz
- configurable high-precision sample clock with a variety of sampling frequencies supported
- 8/16/24/32-bit data width
- synchronous counter in TX mode
- ETM feature
- direct memory access
- standard I2S interface interrupts

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter 12S Controller (I2S).

**Subtitle: Pin Assignment**

The pins for the I2S controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-C5 Series Datasheet](#) > Section IO Pins and [ESP32-C5 Technical Reference Manual](#) > Chapter GPIO Matrix and IO MUX.

**Title: 5.2.1.5 USB Serial/JTAG Controller**

ESP32-C5 contains a USB Serial/JTAG controller. This unit can be used to program the SoC's flash, read program output, as well as attach a debugger to the running program. All of these are possible for any computer with a USB host without any active external components.

**Subtitle: Feature List**

- USB 2.0 full speed compliant, capable of up to 12 Mbit/s transfer speed (note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality
- programming the chip's flash
- CPU debugging with compact JTAG instructions
- a full-speed USB PHY integrated in the chip

For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter USB Serial/JTAG Controller (USB_SERIAL_JTAG).

---

**Footer:**

Espressif Systems  
Page 21  
[Submit Documentation Feedback](#) ESP32-C5-MINI-1 Datasheet v1.0