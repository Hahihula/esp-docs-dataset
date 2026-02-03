**Title: Peripherals**

- **Sampling frequencies**: can be 8 kHz, 16 kHz, 32 kHz, 44.1 kHz, 48 kHz, 88.2 kHz, 96 kHz, 128 kHz, etc.
- Direct Memory Access (DMA)
- A-law and μ-law compression/decompression algorithms for improved signal-to-quantization noise ratio
- Flexible data format control

**Subtitle: Pin Assignment**

The pins for the I2S Controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet > Section 10 Pins](#).

---

**Title: 5.2.1.5 USB Serial/JTAG Controller**

The USB Serial/JTAG controller in the ESP32-C61 chip provides an integrated solution for communicating to the chip over a standard USB CDC-ACM serial port as well as a convenient method for JTAG debugging. It eliminates the need for external chips or JTAG adapters, saving space and reducing cost.

**Subtitle: Feature List**

- **USB 2.0 full speed compliant**, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality
  - CDC-ACM:
    - CDC-ACM adherent serial port emulation (plug-and-play on most modern OSes)
    - Host controllable chip reset and entry into download mode
- **JTAG adapter functionality**:
  - Fast communication with CPU debugging core using a compact representation of JTAG instructions
  - Support for reprogramming of attached flash memory through the ROM startup code
  - Internal PHY

The pins for the USB Serial/JTAG Controller are multiplexed with GPIO12 ~ GPIO13 via IO MUX.

For more information about the pin assignment, see [ESP32-C61 Series Datasheet > Section 10 Pins](#).

---

**Title: 5.2.1.6 LED PWM Controller**

The LED PWM controller can generate independent digital waveform on six channels. The LED PWM controller supports:

- Sampling frequencies
- Direct Memory Access (DMA)
- A-law and μ-law compression/decompression algorithms for improved signal-to-quantization noise ratio

[Footer: Espressif Systems, Submit Documentation Feedback]