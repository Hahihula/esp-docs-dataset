**Title: Functional Description**

---

### Feature List

- Four independent pulse counters with two channels each
- Counter modes: increment, decrement, or disable
- Glitch filtering for input pulse signals and control signals
- Selection between counting on rising or falling edges of the input pulse signal

For details, see [ESP32-C6 Technical Reference Manual](#) > Chapter Pulse Count Controller.

---

### Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

#### Subtitle: USB Serial/JTAG Controller (4.2.1.6)

The USB Serial/JTAG controller in the ESP32-C6 chip provides an integrated solution for communicating to the chip over a standard USB CDC-ACM serial port as well as a convenient method for JTAG debugging. It eliminates the need for external chips or JTAG adapters, saving space and reducing cost.

##### Feature List

- **USB 2.0 full speed compliant**, capable of up to 12 Mbit/s transfer speed (Note that this controller does not support the faster 480 Mbit/s high-speed transfer mode)
- CDC-ACM virtual serial port and JTAG adapter functionality
- **CDC-ACM**:
  - CDC-ACM adherent serial port emulation (plug-and-play on most modern OSes)
  - Host controllable chip reset and entry into download mode

##### Pin Assignment

For details, see Section 2.3.5 Peripheral Pin Assignment.

---

#### Subtitle: Two-wire Automotive Interface (4.2.1.7)

The Two-wire Automotive Interface (TWAI®) is a multi-master, multi-cast communication protocol designed for automotive applications. The TWAI controller facilitates the communication based on this protocol.
  
--- 

**Footer:** Espressif Systems

**Page Number and Document Information:**
- Page 53
- Submit Documentation Feedback 
- ESP32-C6 Series Datasheet v1.4