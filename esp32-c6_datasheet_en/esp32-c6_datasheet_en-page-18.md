**Title: Pins**

---

### Table of Contents

1. **Pin Information**
2. **Power Scheme Details**
3. **Column Pin Settings Explanation**

---

## Page Content:

### 2 PINS

#### Table - Continued from Previous Page (Table 2-2)

| Pin No. | Pin Name       | Pin Type   | Power Providing Pins | Pin Setting At Reset | After Reset    | IO MUX | LP IO MUX | Analog |
|---------|----------------|------------|----------------------|----------------------|---------------|-------|-----------|--------|
| 16      | GPIO12         | IO         | VDDPST2              | IE                   | IE           | IOMUX |          | Analog |
| 17      | GPIO13         | IO         | VDDPST2              | USB PU              | IE, USB PU    | MUX   |          | Analog |
| 18      | GPIO14         | IO         | VDDPST2              | IE                   | IE           | MUX   |          |        |
| 19      | GPIO15         | IO         | VDDPST2              | IE                   | IE           | MUX   |          |        |
| 20      | VDDPST2        | Power      |                      |                      |               |       |           |        |
| 21      | UOTXD          | IO         | VDDPST2              | WPU                 | IOMUX         | MUX   |          |        |
| 22      | UORXD          | IO         | VDDPST2              | IE, WPU             |               |       |           |        |
| 23      | SDIO_CMD       | IO         | VDDPST2              | IOMUX               |               | MUX   |          |        |
| 24      | SDIO_CLK       | IO         | VDDPST2              | WPU                 | IE           | MUX   |          |        |
| 25      | SDIO_DATA0     | IO         | VDDPST2              | IOMUX               |               | MUX   |          |        |
| 26      | SDIO_DATA1     | IO         | VDDPST2              | WPU                 | IE           | MUX   |          |        |
| 27      | SDIO_DATA2     | IO         | VDDPST2              | IOMUX               |               | MUX   |          |        |
| 28      | SDIO_DATA3     | IO         | VDDPST2              | WPU                 | IE           | MUX   |          |        |
| 29      | VDDA1          | Power      |                      |                      |               |       |           |        |
| 30      | XTAL_N         | Analog     |                      |                      |               |       |           |        |
| 31      | XTAL_P         | Analog     |                      |                      |               |       |           |        |
| 32      | VDDA2          | Power      |                      |                      |               |       |           |        |
| 33      | GND            | Power      |                      |                      |               |       |           |        |

---

### Notes:

1. **Bold** marks the pin function set in which a pin has its default function in the default boot mode.
2. In column Pin Providing Power, regarding pins powered by VDD_SPI:
   - Power actually comes from internal power rail supplying power to VDD_SPI.

#### Column Pin Settings

- IE – input enabled
- WPU – internal weak pull-up resistor enabled
- WPD – internal weak pull-down resistor enabled
- USB PU – USB pull-up resistor enabled

##### Default Values:

- By default, the USB function is enabled for USB pins (i.e., GPIO12 and GPIO13), and the pin pull-up or down resistors are decided by the USB pull-up resistor. The USB pull-up resistor control value can be found in `Chapter 10_MUX FUN WPU/WPD`.

##### EFUSEDEPENDS:

- Depends on the value of EFUSE_DIS_PAD_JTAG:
  - 0 – default value, input enabled and internal weak pull-up resistor (IE & WPU)
  - 1 – input enabled

#### Output Enabled
- Output is controlled by `Chapter USB Serial/UTAG`.

---

### Footer Information:

- **Company:** Espressif Systems
- **Document Version:** ESP32-C6 Series Datasheet v1.4
- **Page Number:** 18
- **Feedback Link:** Submit Documentation Feedback

---