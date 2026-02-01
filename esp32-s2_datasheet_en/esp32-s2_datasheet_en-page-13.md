**Title:**
2.2 Pin Overview

**Body Text:**
The ESP32-S2 chip integrates multiple peripherals that require communication with the outside world. To keep the chip package size reasonably small, the number of available pins has to be limited. So the only way to route all the incoming and outgoing signals is through pin multiplexing. Pin muxing is controlled via software programmable registers (see ESP32-S2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix).

All in all, the ESP32-S2 chip has the following types of pins:

- **IO pins** with the following predefined sets of functions to choose from:
  - Each IO pin has predefined IO MUX functions – see Table 2-3 IO MUX Functions
  - Some IO pins have predefined RTC functions – see Table ??
  - Some IO pins have predefined analog functions – see Table 2-8 Analog Functions

**Subtitles and Lists:**
1. **Predefined functions**: means that each IO pin has a set of direct connections to certain signals from on-chip peripherals.
2. During run-time, the user can configure which peripheral signal from a predefined set to connect to a certain pin at a certain time via memory mapped registers.

- Analog pins have exclusively-dedicated analog functions – see Table 2-10 Analog Pins
- Power pins that supply power to the chip components and non-power pins - see Table 2-11 Power Pins

**Table:**
Table 2-1 Pin Overview gives an overview of all the pins. For more information, see the respective sections for each pin type below, or ESP32-S2 Consolidated Pin Overview.

| Pin No | Pin Name       | Pin Type   | Pin Providing Power | Pin Settings At Reset | After Reset |
|--------|----------------|------------|----------------------|-----------------------|-------------|
| 1      | VDDA           | Power      |                      | WPU, IE               | WPU, IE     |
| 2      | LNA_IN         | Analog     |                      |                        |             |
| 3      | VDD3P3        | Power      |                      |                        |             |
| 4      | VDD3P3        | Power      |                      |                        |             |
| 5      | GPIO0          | IO         | VDD3P3_RTC_IO       | WPU, IE               | IO MUX     |
| 6      | GPIO1          | IO         | VDD3P3_RTC_IO       | IE                    | IO MUX     |
| 7      | GPIO2          | IO         | VDD3P3_RTC_IO       | IE                    | Analog      |
| 8      | GPIO3          | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 9      | GPIO4          | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 10     | GPIO5          | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 11     | GPIO6          | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 12     | GPIO7          | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 13     | GPIO8          | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 14     | GPIO9          | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 15     | GPIO10         | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 16     | GPIO11         | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 17     | GPIO12         | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 18     | GPIO13         | IO         | VDD3P3_RTC_IO       | IO MUX               | IO MUX      |
| 19     | GPIO14         | IO         | VDD3P3_RTC_IO       | IE                    | IO MUX      |

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S2 Series Datasheet v1.8