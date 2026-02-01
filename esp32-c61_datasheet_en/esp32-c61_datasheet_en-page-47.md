**Title: Functional Description**

---

### Subtitle: USB Serial/JTAG Controller

The USB Serial/JTAG controller in the ESP32-C61 chip provides an integrated solution for communicating to the chip over a standard USB CDC-ACM serial port as well as a convenient method for JTAG debugging. It eliminates the need for external chips or JTAG adapters, saving space and reducing cost.

**Feature List**
- **USB 2.0 full speed compliant**, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality
    - CDC-ACM:
        - CDC-ACM adherent serial port emulation (plug-and-play on most modern OSes)
        - Host controllable chip reset and entry into download mode
- **JTAG adapter functionality**:
    - Fast communication with CPU debugging core using a compact representation of JTAG instructions
- Support for reprogramming of attached flash memory through the ROM startup code
- Internal PHY

**Pin Assignment**
The pins for the USB Serial/JTAG Controller are multiplexed with GPIO12 ~ GPIO13 via IO MUX.

For more information about the pin assignment, see Section 2.3 IO Pins.

---

### Subtitle: LED PWM Controller

The LED PWM controller can generate independent digital waveform on six channels. The LED PWM controller supports:

**Feature List**
- Generating digital waveform with configurable periods and duty cycle. The resolution of duty cycle can be up to 20 bits
- Multiple clock sources, including 80 MHz PLL clock, external main crystal clock, and internal fast RC oscillator
- Operation when the CPU is in Light-sleep mode
- Gradual increase or decrease of duty cycle, which is useful for the LED RGB color-gradient generator
- Up to 16 duty cycle ranges for gamma curve generation, each can be independently configured in terms of duty cycle direction (increase or decrease), step size, and number of steps

**Pin Assignment**
The pins for the LED PWM Controller can be chosen from any GPIOs via the GPIO Matrix.

---

**Footer:**
Espressif Systems
47 ESP32-C61 Series Datasheet v0.5