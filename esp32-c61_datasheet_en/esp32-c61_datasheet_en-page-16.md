**Title: Pins**

---

**Table Title:** Table 2-1 – cont'd from previous page

| Pin No. | Name       | Type   | Pin Providing Power^2 | At Reset | After Reset | Pin Function Sets^1 |
|---------|-----------|--------|-----------------------|----------|-------------|--------------------|
|         |           |        |                       |          |             |                    |
| 21      | VDDPST2   | Power  | -                     | -        | -           | IO MUX              |
| 22      | SPIQ      | I/O/T  | VDD_SPI/VDDPST2       | -        | -           | IO MUX              |
| 23      | SPIWP     | I/O/T  | VDD_SPI/VDDPST2       | -        | -           | IO MUX              |
| 24      | VDD_SPI   | Power  | VDDPST2               | -        | -           | IO MUX, Analog      |
| 25      | SPIHD     | I/O/T  | VDD_SPI/VDDPST2       | -        | -           | IO MUX              |
| 26      | SPICLK    | O      | VDD_SPI/VDDPST2       | -        | -           | IO MUX              |
| 27      | SPIID     | I/O/T  | VDD_SPI/VDDPST2       | -        | -           | IO MUX, Analog      |
| 28      | USB_D-    | I/O/T  | VDDPST2               | IE       |              | IO MUX, Analog      |
| 29      | USB_D+    | I/O/T  | VDDPST2               | -        | IE,WPU     | IO MUX, Analog      |
| 30      | GPIO24    | I/O/T  | VDDPST2               | -        |              | IO MUX              |
| 31      | GPIO8     | I/O/T  | VDDPST2               | IE       |              | IO MUX, Analog      |
| 32      | GPIO9     | I/O    | VDDPST2               | -        | IE,WPU     | IO MUX, Analog      |
| 33      | UORXD     | I/O/T  | VDDPST2               | -        | IE,WPU     | IO MUX              |
| 34      | UOTXD     | I/O/T  | VDDPST2               | -        | IE,WPU     | IO MUX              |
| 35      | GPIO29    | I/O/T  | VDDPST2               | -        |              | IO MUX, Analog      |
| 36      | GPIO7     | I/O/T  | VDDPST2               | IE       |              | IO MUX              |
| 37      | VDDA1     | Power  | -                     |          |             |                    |
| 38      | XTAL_N    | Analog | -                     |          |             |                    |
| 39      | XTAL_P    | Analog | -                     |          |             |                    |
| 40      | VDDA2     | Power  | -                     |          |             |                    |

---

**Notes:**

1. Bold marks the pin function set in which a pin has its default function in the default boot mode. See Section 3.1 Chip Boot Mode Control.
2. Except for GPIO12 and GPIO13 whose default drive strength is 40 mA, the default drive strength for all other pins is 20 mA.

**Column Pin Settings^1 shows predefined settings at reset and after reset with the following abbreviations:**

- IE – input enabled
- WPU – internal weak pull-up resistor enabled
- WPD – internal weak pull-down resistor enabled
- USB_PU – USB pull-up resistor enabled

- By default, the USB function is enabled for USB pins (i.e., GPIO12 and GPIO13), and the pin pull-up value is decided by the USB pull-up resistor. This resistor is controlled by USB_SERIAL_JTAG_DP/DM/PULLUP and the pull-up value is managed by USB_SERIAL_JTAG_PULLUP_VALUE.

- When the USB function is disabled, USB pins are used as regular GPIOs and the pin's internal weak pull-up and pull-down resistors are disabled by default (configurable by IO_MUXFUN_WPU/WPD).

---

**Footer:**
Espressif Systems
ESP32-C61 Series Datasheet v0.5

Page 16