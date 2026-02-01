**Title: Functional Description**

---

### Pin Assignment

The pins for the I2S Controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

---

#### **4.2.1.5 Pulse Count Controller**

The Pulse Count Controller (PCNT) is designed to count input pulses by tracking the rising and falling edges of the input pulse signal.

**Feature List**
- Four independent pulse counters with two channels each
- Counter modes: increment, decrement, or disable
- Glitch filtering for input pulse signals and control signals
- Selection between counting on rising or falling edges of the input pulse signal

For details, see ESP32-H2 Technical Reference Manual > Chapter Pulse Count Controller (PCNT).

---

### Pin Assignment

The pins for the Pulse Count Controller can be chosen from any GPIOs via the GPIO Matrix.

For more information about the pin assignment, see Section 2.3 IO Pins and ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

---

#### **4.2.1.6 USB Serial/JTAG Controller**

The USB Serial/JTAG controller in the ESP32-H2 chip provides an integrated solution for communicating to the chip over a standard USB CDC-ACM serial port as well as a convenient method for JTAG debugging. It eliminates the need for external chips or JTAG adapters, saving space and reducing cost.

**Feature List**
- USB 2.0 full speed compliant, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality
- **CDC-ACM:**
  - CDC-ACM adherent serial port emulation (plug-and-play on most modern OSes)
  - Host controllable chip reset and entry into download mode
- **JTAG adapter functionality:** 
  - Fast communication with CPU debugging core using a compact representation of JTAG instructions
  - Internal PHY

---

**Footer:**
Espressif Systems  
43  
Submit Documentation Feedback  
ESP32-H2 Series Datasheet v1.2