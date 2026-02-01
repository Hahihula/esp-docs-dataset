**Title: Functional Description**

---

### Pin Assignment

The pins for the LP I2S controller can be chosen from any LP GPIOs via the LP GPIO Matrix.

#### Subtitle 4.2.2.8 Pulse Count Controller (PCNT)

The pulse count controller (PCNT) is designed to count input pulses.

##### Feature List
- Four independent pulse counters (units) that count from 1 to 65535.
- Each unit consists of two independent channels sharing one pulse counter.
- All channels have input pulse signals with their corresponding control signals.
- Independently filter glitches of input pulse signals and control signals on each unit.
- Each channel has the following parameters:
  - Selection between counting on rising or falling edges of the input pulse signal
  - Configuration to Increment, Decrement, or Disable counter mode for control signal’s high and low states.

##### Additional Information

Maximum frequency of pulses: \( \frac{f_{APB_CLK}}{2} \)

---

### Pin Assignment (Repeated from above section due to layout overlap in the image.)

#### Subtitle 4.2.2.9 USB 2.0 High-Speed OTG

The ESP32-P4 chip features a USB 2.0 High-Speed On-The-Go peripheral (OTG_HS) with an integrated transceiver. This OTG_HS complies with the USB 2.0 specification, OTG Revision 1.3, and OTG Revision 2.0 specifications. The interface supports USB 2.0 High-Speed mode (480 Mbit/s), Full-Speed mode (12 Mbit/s), and Low-Speed mode (1.5 Mbit/s).

##### Feature List
- When OTG_HS operates in High-Speed or Full-Speed modes, it can be configured as either a Host or a Device.
- When OTG_HS operates in Low-Speed mode, it can only be configured as a Host.

---

### General Features

USB 2.0 specification, OTG Revision 1.3 and OTG Revision 2.0 specifications
High-Speed, Full-Speed, and Low-Speed data rates
As a host and a device in High-Speed mode and Full-Speed mode.
Dynamic FIFO (DFIFO) sizing, each device EP/host channel can dynamically allocate a maximum of 4 KB FIFO.
Multiple modes of memory access

---

**Footer:**
Espressif Systems  
67  
ESP32-P4 Series Datasheet v0.6  

[Submit Documentation Feedback](#)