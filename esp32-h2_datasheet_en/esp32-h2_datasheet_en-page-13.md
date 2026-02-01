**Title:**
2 Pins

**Subtitle:**
2.2 Pin Overview

**Body Text:**

The ESP32-H2 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers (see ESP32-H2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix).

All in all, the ESP32-H2 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-3 IO MUX Pin Functions
  - Some IO pins have predefined analog functions – see Table 2-5 Analog Functions

Predefined functions means that each IO pin has a set of direct connections to certain signals from on-chip components. During run-time, the user can configure which component signal from a predefined set to connect to a certain pin at a certain time via memory mapped registers.

- **Analog pins** that have exclusively-dedicated analog functions – see Table 2-6 Analog Pins

- **Power pins** that supply power to the chip components and non-power pins – see Table 2-7 Power Pins

Depending on whether can work in Deep-sleep mode or Light-sleep mode, the pins of ESP32-H2 can also be divided into:

- Digital pins (GPIO0 ~ GPIO5, GPIO16 ~ GPIO27): are unable to work in Deep-sleep mode, but can work in Light-sleep mode only if the power domain controlled by the XPD TOP does not power off.

- LP pins (GPIO8 ~ GPIO14): are able to work in any chip mode.

**Table:**
Table 2-1 Pin Overview

| Pin No. | Pin Name       | Pin Type    | Power Providing | Pin Settings At Reset | After Reset   | Pin Function Sets |
|---------|---------------|-------------|------------------|------------------------|---------------|--------------------|
|         |               |             |                  |                        |               |                    |
| 1       | VDD3P3        | Power       | 2                |                         |               |                    |
| 2       | VDD3P3        | Power       |                  |                         | IO MUX        |                    |
| 3       | GPIO0         | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 4       | GPIO1         | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 5       | MTMS          | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 6       | MTDO          | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 7       | MTCK          | IO          | VDDPST1          | IE^4                    | IO MUX        | Analog              |
| 8       | MTDI          | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 9       | VDDPST1       | Power       |                  |                         |               |                    |
| 10      | GPIO8         | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 11      | GPIO9         | IO          | VDDPST1          | IE, WPU                | IO MUX        | Analog              |
| 12      | GPIO10        | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 13      | GPIO11        | IO          | VDDPST1          | IE                      | IO MUX        | Analog              |
| 14      | GPIO12        | IO          | VDDA_PMU/VBAT     |                         | IO MUX        |                    |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-H2 Series Datasheet v1.2