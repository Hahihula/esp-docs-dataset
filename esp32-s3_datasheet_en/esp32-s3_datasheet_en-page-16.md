**Title:**
2 Pins

**Subtitle:**
2.2 Pin Overview

**Body Text:**

The ESP32-S3 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers (see ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO Matrix).

All in all, the ESP32-S3 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-4 IO MUX Functions
  - Some IO pins have predefined RTC functions – see Table 2-6 RTC Functions
  - Some IO pins have predefined analog functions – see Table 2-8 Analog Functions

Predefined functions means that each IO pin has a set of direct connections to certain on-chip peripherals. During run-time, the user can configure which peripheral from a predefined set to connect to a certain pin at a certain time via memory mapped registers (see ESP32-S3 Technical Reference Manual > Chapter IO MUX and GPIO pins).

- Analog pins that have exclusively-dedicated analog functions – see Table 2-10 Analog Pins
- Power pins that supply power to the chip components and non-power pins – see Table 2-11 Power Pins

**Table:**
Table 2-1 Pin Overview gives an overview of all the pins. For more information, see the respective sections for each pin type below, or ESP32-S3 Consolidated Pin Overview.

**Table Title:**
Table 2-1. Pin Overview

| Pin No | Pin Name       | Pin Type    | Pin Providing Power | Pin Settings At Reset | Pin Settings After Reset | Pin Function Sets |
|--------|----------------|-------------|----------------------|-----------------------|----------------------------|--------------------|
| 1      | LNA_IN         | Analog     | VDD3P3              | WPU, IE               | WPU, IE                    | IO MUX             |
| 2      | VDD3P3        | Power       |                      |                       |                            | RTC IO MUX         |
| 3      | VDD3P3        | Power       |                      |                       |                            | Analog             |
| 4      | CHIP PU       | Analog     | VDD3P3_RTC          | WPU, IE               | WPU, IE                    | IO MUX             |
| 5      | GPIO0         | IO          | VDD3P3              |                      |                            | RTC IO MUX         |
| 6      | GPIO1         | IO          | VDD3P3              |                      |                            | Analog             |
| 7      | GPIO2         | IO          | VDD3P3              |                      |                            | Analog             |
| 8      | GPIO3         | IO          | VDD3P3              |                      |                            | Analog             |
| 9      | GPIO4         | IO          | VDD3P3              |                      |                            | Analog             |
| 10     | GPIO5         | IO          | VDD3P3              |                      |                            | Analog             |
| 11     | GPIO6         | IO          | VDD3P3              |                      |                            | Analog             |
| 12     | GPIO7         | IO          | VDD3P3              |                      |                            | Analog             |
| 13     | GPIO8         | IO          | VDD3P3              |                      |                            | Analog             |
| 14     | GPIO9         | IO          | VDD3P3              |                      |                            | Analog             |
| 15     | GPIO10        | IO          | VDD3P3              |                      |                            | Analog             |
| 16     | GPIO11        | IO          | VDD3P3              |                      |                            | Analog             |
| 17     | GPIO12        | IO          | VDD3P3              |                      |                            | Analog             |
| 18     | GPIO13        | IO          | VDD3P3              |                      |                            | Analog             |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 Series Datasheet v2.1