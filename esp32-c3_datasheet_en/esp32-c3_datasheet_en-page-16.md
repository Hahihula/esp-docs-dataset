**Title:**
2 Pins

**Subtitle:**
2.2 Pin Overview

**Body Text:**

The ESP32-C3 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers (see ESP32-C3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix).

All in all, the ESP32-C3 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-4 IO MUX Pin Functions
  - Some IO pins have predefined analog functions – see Table 2-6 Analog Functions

Predefined functions means that each IO pin has a set of direct connections to certain signals from on-chip peripherals. During run-time, the user can configure which peripheral signal from a predefined set to connect to a certain pin at a certain time via memory mapped registers.

- **Analog pins** that have exclusively-dedicated analog functions – see Table 2-8 Analog Pins
- **Power pins** that supply power to the chip components and non-power pins – see Table 2-9 Power Pins

**Table:**
Table 2-1 Pin Overview gives an overview of all the pins. For more information, see the respective sections for each pin type below, or ESP32-C3 Consolidated Pin Overview.

| Pin No. | Pin Name       | Pin Type | Pin Providing    | Pin Settings At Reset | Pin Function Sets After Reset |
|---------|---------------|----------|------------------|-----------------------|--------------------------------|
| 1       | LNA_IN        | Analog   | Power            | -                     | IO MUX                          |
| 2       | VDD3P3       | Power    |                  | -                     | -                              |
| 3       | VDD3P3       | Power    |                  | -                     | -                              |
| 4       | XTAL_32K_P   | IO       | VDD3P3_RTC      | IE                    | IO MUX                          |
| 5       | XTAL_32K_N   | IO       | VDD3P3_RTC      | IE                    | IO MUX                          |
| 6       | GPIO02       | IO       | VDD3P3_RTC      | IE                    | IO MUX                          |
| 7       | CHIP_EN      | Analog   |                  | -                     | IO MUX                          |
| 8       | GPIO03       | IO       | VDD3P3_RTC      | IE                    | IO MUX                          |
| 9       | MTMS         | IO       | VDD3P3_RTC      | IE                    | IO MUX                          |
| 10      | MTDI         | IO       | VDD3P3_RTC      | IE                    | IO MUX                          |
| 11      | VDD3P3_RTC   | Power    |                  | -                     | -                              |
| 12      | MTCK         | IO       | VDD3P3_CPU      | IE                    | IO MUX                          |
| 13      | MTDO         | IO       | VDD3P3_CPU      | IE                    | IO MUX                          |
| 14      | GPIO08       | IO       | VDD3P3_CPU      | IE                    | IO MUX                          |
| 15      | GPIO09       | IO       | VDD3P3_CPU      | IE, WPU               | IO MUX                          |
| 16      | GPIO10       | IO       | VDD3P3_CPU      | IE                    | IO MUX                          |
| 17      | VDD3P3_CPU   | Power    |                  | -                     | -                              |
| 18      | VDD_SPI      | Power    | VDD3P3_CPU      | WPU                   | IO MUX                          |
| 19      | SPIHD        | IO       | VDD_SPI / VDD3P3_CPU | IE, WPU               | IO MUX                          |
| 20      | SPIWP        | IO       | VDD_SPI / VDD3P3_CPU | WPU                   | IO MUX                          |

**Footer:**
Espressif Systems
ESP32-C3 Series Datasheet v2.2

Submit Documentation Feedback