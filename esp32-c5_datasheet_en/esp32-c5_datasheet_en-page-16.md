**Title:**
2 Pins

**Subtitle:**
2.2 Pin Overview

**Body Text:**

The ESP32-C5 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers. For details, see ESP32-C5 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

All in all, the ESP32-C5 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-3 IO MUX Pin Functions
  - Some IO pins have predefined LP IO MUX functions – see Table 2-5 LP IO MUX Functions
  - Some IO pins have predefined analog functions – see Table 2-7 Analog Functions

Predefined functions means that each IO pin has a set of direct connections to certain signals from on-chip components. During run-time, the user can configure which component signal from a predefined set to connect to a certain pin at a certain time via memory mapped registers.

- **Analog pins** have exclusively-dedicated analog functions – see Table 2-8 Analog Pins
- Power pins supply power to the chip components and non-power pins - see Table 2-9 Power Pins

**Table:**
Table 2-1 Pin Overview gives an overview of all the pins. For more information, see respective sections below.

Alternatively, see Appendix A – ESP32-C5 Consolidated Pin Overview.
Table 2-1. Pin Overview
| No. | Pin Name | Type | Pin Providing Power (2-4) | Pin Settings At Reset | After Reset |
|-----|----------|------|----------------------------|------------------------|------------|
| 1   | VDDA6    | Power |                           |                        |            |
| 2   | GND      | Power |                           |                        |            |
| 3   | VDDA7    | Power |                           |                        |            |
| 4   | XTAL_N   | Analog |                          |                        |            |
| 5   | XTAL_P   | Analog |                          |                        |            |
| 6   | VDDAS8   | Power |                           |                        |            |
| 7   | CHIP PU  | Analog | VDDPST1                    |                        |            |
| 8   | VDDPST1  | Power |                           |                        |            |
| 9   | XTAL_32K_P | IO    | VDDPST1                    |                        |            |
| 10  | XTAL_32K_N | IO    | VDDPST1                    |                        |            |
| 11  | MTMS     | IO    | VDDPST1, IE               | IE                     |            |
| 12  | MTDI     | IO    | VDDPST1, IE               | IE                     |            |
| 13  | MTCK     | IO    | VDDPST1                    | IE, WPU                |            |
| 14  | MTDO     | IO    | VDDPST1                    |                        |            |
| 15  | GPIO6    | IO    | VDDPST1                    |                        |            |
| 16  | GPIO7    | IO    | VDDPST1                    |                        |            |
| 17  | GPIO8    | IO    | VDDPST1                    |                        |            |
| 18  | GPIO9    | IO    | VDDPST1                    |                        |            |
| 19  | GPIO10   | IO    | VDDPST1                    |                        |            |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-C5 Series Datasheet v1.0