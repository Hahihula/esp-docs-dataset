**Title:**
2 Pins

**Subtitle:**
2.2 Pin Overview

**Body Text:**

The ESP32-C6 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers (see ESP32-C6 Technical Reference Manual > Chapter IO MUX and GPIO Matrix).

All in all, the ESP32-C6 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-4 QFN40 IO MUX Pin Functions or Table 2-5 QFN32 IO MUX Pin Functions
  - Some IO pins have predefined LP IO MUX functions – see Table 2-7 LP IO MUX Functions
  - Some IO pins have predefined analog functions – see Table 2-9 Analog Functions

Predefined functions means that each IO pin has a set of direct connections to certain signals from on-chip peripherals. During run-time, the user can configure which peripheral signal from a predefined set to connect to a certain pin at a certain time via memory mapped registers.

- **Analog pins** that have exclusively-dedicated analog functions – see Table 2-12 Analog Pins
- **Power pins** that supply power to the chip components and non-power pins – see Table 2-13 Power Pins

Table 2-1 QFN40 Pin Overview or Table 2-2 QFN32 Pin Overview gives an overview of all the pins. For more information, see the respective sections for each pin type below, or ESP32-C6 Consolidated Pin Overview.

**Table:**
Table 2-1. QFN40 Pin Overview

| Pin No. | Pin Name       | Pin Type | Pin Providing Power (2, 3) | Pin Settings At Reset | After Reset | Pin Function Sets |
|---------|---------------|----------|----------------------------|-----------------------|-------------|--------------------|
| 1       | ANT           | Analog   |                           |                       |             | IO MUX            |
| 2       | VDDA3P3      | Power    |                           |                       |             |                   |
| 3       | VDDA3P3      | Power    |                           |                       |             |                   |
| 4       | CHIP_PU      | Analog   | VDDPST1                    |                       |             |                   |
| 5       | VDDPST1      | Power    |                           |                       |             | IO MUX            |
| 6       | XTAL_32K_P   | IO       | VDDPST1                    |                       |             | Analog            |
| 7       | XTAL_32K_N   | IO       | VDDPST1                    |                       |             | IO MUX            |
| 8       | GPIO02       | IO       | VDDPST1                    | IE                     | IE          | LP IO MUX         |
| 9       | GPIO03       | IO       | VDDPST1                    | IE                     | IE          | Analog            |
| 10      | MTMS         | IO       | VDDPST1                    | IE                     | IE          | IO MUX            |
| 11      | MTDI         | IO       | VDDPST1                    | IE                     | IE          | IO MUX            |
| 12      | MTCK         | IO       | VDDPST1                    | IE, WPU^5           |             | IO MUX            |
| 13      | MTDO         | IO       | VDDPST1                    | IE                     | IE          | IO MUX            |
| 14      | GPIO8        | IO       | VDDPST2                    | IE                     | IE          | IO MUX            |
| 15      | GPIO9        | IO       | VDDPST2                    | IE, WPU              | IE, WPU    | IO MUX            |
| 16      | GPIO10       | IO       | VDDPST2                    | IE                     | IE          | IO MUX            |
| 17      | GPIO11       | IO       | VDDPST2                    | IE                     | IE          | IO MUX            |

**Footer:**
Espressif Systems
Submit Documentation Feedback

Series Datasheet v1.4