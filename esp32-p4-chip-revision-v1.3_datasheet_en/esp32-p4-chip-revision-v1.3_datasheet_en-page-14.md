**Title:**
2.2 Pin Overview

**Body Text:**

The ESP32-P4 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers (see ESP32-P4 Technical Reference Manual > Chapter GPIO Matrix and IO MUX). In addition, ESP32-P4 has a number of pins that are dedicated to certain peripherals, such as MIPI DSI and CSI, and cannot be used for general-purpose IO.

All in all, the ESP32-P4 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-3 IO MUX Functions
  - Some IO pins have predefined LP IO MUX functions – see Table 2-5 LP IO MUX Functions
  - Some IO pins have predefined analog functions – see Table 2-7 Analog Functions

Predefined functions mean that each IO pin has a set of direct connections to certain signals from on-chip components. During run-time, the user can configure which component signal from a predefined set to connect to a certain pin at a certain time via memory mapped registers.

**Subsections:**
1. **Dedicated interface pins** can only be used by such peripherals; see Table 2-9 Dedicated Interface Pins
2. **Analog pins** that have exclusively-dedicated analog functions – see Table 2-10 Analog Pins
3. **Power pins** that supply power to the chip components and non-power pins – see Table 2-11 Power Pins

**Table:**
Table 2-1 Pin Overview gives an overview of all the pins. For more information, see the respective sections for each pin type below, or Appendix A – ESP32-P4 Consolidated Pin Overview.

| **Pin No.** | **Pin Name**       | **Pin Type** | **Power**      | **Pin Providing Power 1, 2, 3** | **Pin Settings At Reset** | **After Reset** |
|-------------|--------------------|--------------|----------------|----------------------------------|----------------------------|-------------------|
| 1           | GPIO01             | IO           | VDD_LP / VDD_BAT | -                                | IO MUX                   | LP IO MUX         |
| 2           | GPIO02             | IO           | VDD_LP / VDD_BAT | IE, WPU5                        | IO MUX                   | LP IO MUX         |
| 3           | GPIO03             | IO           | VDD_LP / VDD_BAT | -                                | IO MUX                   | LP IO MUX         |
| 4           | GPIO04             | IO           | VDD_LP                     | IE                               | IO MUX                   | LP IO MUX         |
| ...        | ...                | ...          | ...              | ...                              | ...                      | ...               |

**Footer:**
Espressif Systems
ESP32-P4 Series Datasheet v0.6

Submit Documentation Feedback