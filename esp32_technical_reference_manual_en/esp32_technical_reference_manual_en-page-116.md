**Chapter Title:**
Chapter 6 IO MUX and GPIO Matrix (GPIO, IO MUX)

**Body Text:**

1. **Introduction to IO MUX Functionality:** 
   - When connected directly or through a function bypassing the GPIO matrix.
   - High-speed digital functions can use this for better high-frequency performance.

2. **GPIO Matrix Description:**
   - Full-switching matrix between peripheral input/output signals and pins:
     - For input, each of 162 internal peripherals selects any GPIO pin as an input source.
     - For output from the chip; one of 34 GPIO pins can be connected to a subset (176) of peripheral outputs.

3. **RTC IO MUX Functionality:**
   - Connects GPIO pins for low-power and analog functions, with specific "RTC" options:
     - Reference Section [6.9](#section-6.9) for details on GPIO matrix peripherals.
     - Reference Section [6.11](#section-6.11) for RTC IO MUX function specifics.

**Figure Description:**
- **Figure 6.1-2:** Internal Structure of a Pad
   - Shows the internal structure with components like IE, VDD3P3, WPU, OE, Buf, WPD, and GND.
   - Describes routing to/from peripherals through bonding pads for physical connections.

**Legend:**
- **IE**: Input enable (Bonding pad)
- **OE**: Output enable
- **WPU**: Internal weak pull-up resistor
- **WPD**: Internal weak pull-down resistor

**Footer Information:** 
- Company Name: Espressif Systems
- Document Version and Submission Link:
  - ESP32 TRM (Version 5.6)  
  - Submit Documentation Feedback