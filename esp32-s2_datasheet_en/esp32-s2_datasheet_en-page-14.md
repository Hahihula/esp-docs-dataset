**Title: Pins**

---

**Subtitle: Cont'd from previous page**

| Pin No. | Pin Name       | Pin Type   | Pin Providing Power^2,3,4 | At Reset    | After Reset  | IO MUX | Pin Function Sets |
|---------|---------------|------------|---------------------------|-------------|--------------|-------|-------------------|
| 20      | VDD3P3_RTC   | Power      | VDD3P3_RTC_IO            |             |              | IO MUX | RTC IO MUX Analog |
| 21      | XTAL_32K_P    | IO         | VDD3P3RTC_IO              |             |              | IO MUX | RTC IO MUX Analog |
| 22      | XTAL_32K_N    | IO         | VDD3P3_RTC_IO             |             |              | IO MUX | RTC IO MUX Analog |
| 23      | DAC_1         | IO         | VDD3P3_RTC_IO             | IE          |               |       |                   |
| 24      | DAC_2         | IO         | VDD3P3_RTC_IO             | IE          |               |       |                   |
| 25      | GPIO19        | IO         | VDD3P3_RTC_IO             |              |               |       |                   |
| 26      | GPIO20        | IO         | VDD3P3_RTC_IO             |              |               |       |                   |
| 27      | VDD3P3_RTC_IO | Power      | VDD3P3RTC_IO              |             |              | IO MUX | RTC IO MUX Analog |
| 28      | GPIO21        | IO         | VDD3P3_RTC_IO             |             |              | IO MUX | RTC IO MUX Analog |
| 29      | SPICS1        | IO         | VDD_SPI                  | WPU, IE    | WPU, IE      |       |                   |
| 30      | VDD_SPI       | Power      | VDD_SPI                  |             |              |       |                   |
| 31      | SPIHD         | IO         | VDD_SPI                  | WPU, IE    | WPU, IE      |       |                   |
| 32      | SPIWP         | IO         | VDD_SPI                  | WPU, IE    | WPU, IE      |       |                   |
| 33      | SPICSO        | IO         | VDD_SPI                  | WPU, IE    | WPU, IE      |       |                   |
| 34      | SPICLK        | IO         | VDD_SPI                  | WPU, IE    | WPU, IE      |       |                   |
| 35      | SPIQ          | IO         | VDD_SPI                  | WPU, IE    | WPU, IE      |       |                   |
| 36      | SPID          | IO         | VDD_SPI                  | WPU, IE    | WPU, IE      |       |                   |
| 37      | GPIO33        | IO         | VDD SPI/VDD3P3_CPU        | IE         |               |       |                   |
| 38      | GPIO34        | IO         | VDD SPI/VDD3P3_CPU        | IE         |               |       |                   |
| 39      | GPIO35        | IO         | VDD SPI/VDD3P3_CPU        | IE         |               |       |                   |
| 40      | GPIO36        | IO         | VDD SPI/VDD3P3_CPU        | IE         |               |       |                   |
| 41      | GPIO37        | IO         | VDD SPI/VDD3P3_CPU        | IE         |               |       |                   |
| 42      | GPIO38        | IO         | VDD3P3_CPU                | IE         |               |       |                   |
| 43      | MTCK          | IO         | VDD3P3_CPU                | IE^6       |               |       |                   |
| 44      | MTDO          | IO         | VDD3P3_CPU                | IE         |               |       |                   |
| 45      | VDD3P3_CPU    | Power      | VDD3P3CPU                 | IE         |               |       |                   |
| 46      | MTDI          | IO         | VDD3P3_CPU                | IE         |               |       |                   |
| 47      | MTMS           | IO         | VDD3P3_CPU                | IE         |               |       |                   |
| 48      | UOTXD         | IO         | VDD3P3_CPU                | WPU, IE    | WPU, IE      |       |                   |
| 49      | UORXD         | IO         | VDD3P3_CPU                |             |              |       |                   |
| 50      | GPIO45        | Power      | VDD3P3CPU                 | WPD, IE    | WPD, IE      |       |                   |
| 51      | VDDA          | Power      |                          |            |              |       |                   |
| 52      | XTAL_N        | Analog      |                          |            |              |       |                   |
| 53      | XTAL_P        | Analog      |                          |            |              |       |                   |
| 54      | VDDA          | Power      |                          | WPD, IE    | WPD, IE      | IO MUX |                   |
| 55      | GPIO46        | IO         | VDD3P3_CPU                |             |              |       |                   |
| 56      | CHIP_PU       | Analog      | VDD3P3_RTC_IO             |             |              |       |                   |

---

**Footnotes:**

1. Bold marks the pin function set in which a pin has its default function in the default boot mode.
2. See Section **3.1 Chip Boot Mode Control**.

3. In column Pin Providing Power, regarding pins powered by VDD3P3_CPU / VDD_SPI:
   - Pin Providing Power (either VDD3P3_CPU or VDD_SPI) can be configured via a register; see ESP32-S2 Technical Reference Manual > Chapter IO MUX and GPIO Matrix.

4. Default drive strength for all IO pins is 20 mA.

---

**Footer:**

- Espresso Systems
- Submit Documentation Feedback

**Page Number:** 

14

**Document Title:** 

ESP32-S2 Series Datasheet v1.8