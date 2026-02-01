**Title: Pins**

---

**Subtitle: Cont'd from previous page**

| Pin No. | Pin Name       | Pin Type | Pin Providing Power         | At Reset   | After Reset  | Pin Function Sets    |
|---------|---------------|----------|------------------------------|------------|--------------|----------------------|
|         |               |          |                              |            |              |                     |
| 19      | GPIO14        | IO       | VDD3P3_RTC                   | IE         | IO MUX       | RTC IO MUX Analog   |
| 20      | VDD3P3_RTC    | Power    |                              |            |              |                      |
| 21      | XTAL_32K_P    | IO       | VDD3P3_RTC                   | IE         | IO MUX       | RTC IO MUX Analog   |
| 22      | XTAL_32K_N    | IO       | VDD3P3_RTC                   | IE         | IO MUX       | RTC IO MUX Analog   |
| 23      | GPIO17        | IO       | VDD3P3_RTC                   | IE         | IO MUX       | RTC IO MUX Analog   |
| 24      | GPIO18        | IO       | VDD3P3_RTC                   | IE         | IO MUX       | RTC IO MUX Analog   |
| 25      | GPIO19        | IO       | VDD3P3RTC                    | IE         | IO MUX       | RTC IO MUX Analog   |
| 26      | GPIO20        | IO       | VDD3P3_RTC                   |            |              |                      |
| 27      | GPIO21        | IO       | VDD3P3_RTC                   | WPU, IE    | WPU, IE      | RTC IO MUX Analog   |
| 28      | SPICS1        | IO       | VDD_SPI                      |            |              |                      |
| 29      | VDD_SPI       | Power    |                              |            |              |                      |
| 30      | SPIHD         | IO       | VDD_SPI                      | WPU, IE    | WPU, IE      | RTC IO MUX Analog   |
| 31      | SPiWP         | IO       | VDD_SPI                      | WPU, IE    | WPU, IE      | IO MUX              |
| 32      | SPICSO        | IO       | VDD_SPI                      |            |              |                      |
| 33      | SPICLK        | IO       | VDD_SPI                      | WPU, IE    | WPU, IE      | IO MUX              |
| 34      | SPIQ          | IO       | VDD_SPI                      | WPU, IE    | WPU, IE      | IO MUX              |
| 35      | SPID          | IO       | VDD_SPI                      |            |              |                      |
| 36      | SPICLK_N      | IO       | VDD_SPI/VDD3P3_CPU           | IE         | IO MUX       | IO MUX              |
| 37      | SPICLK_P      | IO       | VDD_SPI/VDD3P3_CPU           | IE         | IO MUX       | IO MUX              |
| 38      | GPIO33        | IO       | VDD_SPI/VDD3P3_CPU           |            |              |                      |
| 39      | GPIO34        | IO       | VDD_SPI/VDD3P3_CPU           | IE         | IO MUX       | IO MUX              |
| 40      | GPIO35        | IO       | VDD_SPI/VDD3P3_CPU           |            |              |                      |
| 41      | GPIO36        | IO       | VDD_SPI/VDD3P3_CPU           | IE         | IO MUX       | IO MUX              |
| 42      | GPIO37        | IO       | VDD_SPI/VDD3P3_CPU           |            |              |                      |
| 43      | GPIO38        | IO       | VDD3P3_CPU                    | IE         | IO MUX       | IO MUX              |
| 44      | MTCK          | IO       | VDD3P3_CPU                    | IE         | IO MUX       | IO MUX              |
| 45      | MTDO          | IO       | VDD3P3_CPU                    |            |              |                      |
| 46      | VDD3P3_CPU    | Power    |                              | WPU, IE    | WPU, IE      | RTC IO MUX Analog   |
| 47      | MTDI          | IO       | VDD3P3_CPU                    |            |              |                      |
| 48      | MTMS          | IO       | VDD3P3_CPU                    |            |              |                      |
| 49      | UOTXD         | IO       | VDD3P3_CPU                    | WPU, IE    | WPU, IE      | IO MUX              |
| 50      | UORXD         | IO       | VDD3P3_CPU                    |            |              |                      |
| 51      | GPIO45        | IO       | VDD3P3_CPU                    | WPU, IE    | WPU, IE      | IO MUX              |
| 52      | GPIO46        | IO       | VDD3P3_CPU                    |            |              |                      |
| 53      | XTAL_N        | Analog   |                              | WPD, IE    | WPD, IE      | IO MUX              |
| 54      | XTAL_P        | Analog   |                              |            |              |                      |
| 55      | VDDA          | Power    |                              |            |              |                      |
| 56      | VDD           | Power    |                              |            |              |                      |
| 57      | GND           | Power    |                              |            |              |                      |

**Footnotes:**
1. Bold marks the pin function set in which a pin has its default function in the default boot mode.
2. In column Pin Providing Power, regarding pins powered by VDD_SPI:
   - Power actually comes from the internal power rail supplying power to VDD_SPI. For details, see Section 25.2 Power Scheme.

**Additional Information:**
- ESP32-S3 Series Datasheet v2.1
- Submit Documentation Feedback

---

*Note: The text in bold is used for emphasis and indicates specific information about the pin function sets.*