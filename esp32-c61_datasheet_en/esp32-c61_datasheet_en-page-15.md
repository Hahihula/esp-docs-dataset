**Title:**
2 Pins

**Subtitle:**
2.2 Pin Overview

**Body Text:**

The ESP32-C61 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers.

All in all, the ESP32-C61 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-3 IO MUX Functions
  - Some IO pins have predefined LP IO MUX functions – see Table 2-4 LP IO MUX Functions
  - Some IO pins have predefined analog functions – see Table 2-6 Analog Functions

Predefined functions means that each IO pin has a set of direct connections to certain signals from on-chip peripherals. During run-time, the user can configure which peripheral signal from a predefined set to connect to a certain pin at a certain time via memory mapped registers.

- **Analog pins** that have exclusively-dedicated analog functions – see Table 2-7 Analog Pins
- Power pins that supply power to the chip components and non-power pins – see Table 2-8 Power Pins

**Table Descriptions:**

1. **Table 2-1 Pin Overview**: Provides an overview of all the pins.
   - Columns include:
     - Pin No.: Lists pin numbers from ANT_2G (pin number 1) to SPICSO (pin number 20).
     - Name: Names corresponding IO or power functions for each pin, such as VDDA3, VDDPST1, etc.

2. **Table 2-6 Analog Functions**: Lists predefined analog pins.
   - Columns include:
     - Pin No.: Lists the same range of pin numbers from ANT_2G to SPICSO (same structure and columns).

3. **Table 2-8 Power Pins**: Lists power supply-related IO functions for each corresponding chip component or non-power function, such as VDDA3, VDDPST1.

**Footer:**
Espressif Systems
ESP32-C61 Series Datasheet v0.5

**Page Number:** 
15