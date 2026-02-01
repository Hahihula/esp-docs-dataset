**Title: Pins**

---

### Table of Contents

- **Table 2-1 – continued from previous page**
  - Pin No.
  - Name
  - Type (Pin)
  - Power Providing At Reset | After Reset Set |
  - Pin Function Sets |

| Pin No. | Name          | Pin Type   | Pin Providing    | Pin Settings         | Pin Function Sets |
|---------|--------------|-----------|------------------|----------------------|--------------------|
| 15      | XTAL_32K_P   | IO        | VDDA_PMU/VBAT    |                      | IO MUX             |
| 16      | XTAL_32K_N   | IO        | VDDA_PMU/VBAT    |                      | IO MUX             |
| 17      | CHIP_EN      | Analog    |                   | VBAT                 | IO MUX             |
| 18      | VBAT         | Power     |                   |                      |                    |
| 19      | VDDA_PMU     | Power     |                   |                      |                    |
| 20      | VDDPST2      | Power     |                   |                      | IO MUX             |
| 21      | GPIO22       | IO        | VDDPST2          | IE, WPU              | IO MUX             |
| 22      | UORXD        | IO        | VDDPST2          | IE, WPU              | IO MUX             |
| 23      | UOTXD        | IO        | VDDPST2          | IE, WPU              | IO MUX             |
| 24      | GPIO25       | IO        | VDDPST2          | IE                   | IO MUX             |
| 25      | GPIO26       | IO        | VDDPST2          | IE                   | Analog             |
| 26      | GPIO27       | IO        | VDDPST2          | IE, USB_LPU         | IO MUX             |
| 27      | VDD3P3       | Power     |                   |                      |                    |
| 28      | XTAL_N       | Analog    |                   |                      |                    |
| 29      | XTAL_P       | Analog    |                   |                      |                    |
| 30      | VDD3P3       | Power     |                   |                      |                    |
| 31      | VDD3P3       | Power     |                   |                      |                    |
| 32      | ANT          | analog    |                   |                      |                    |
| 33      | GND          |           |                  |                      |                    |

---

### Notes

- **Bold** marks the pin function set in which a pin has its default function in the default boot mode. See Section [3.1 Chip Boot Mode Control](#).
  
- Default drive strength for GPIO26 and GPIO27 is 40 mA, and 20 mA for the other GPIOs.

### Column Pin Settings

Column **Pin Settings** shows predefined settings at reset and after reset with the following abbreviations:

- IE – input enabled
- WPU – internal weak pull-up resistor enabled
- WPD – internal weak pull-down resistor enabled
- USB_PU – USB pull-up resistor enabled
  
  - By default, the USB function is enabled for USB pins (i.e., GPIO26 and GPIO27), and the pin pull-up or pull-down resistors are disabled by the USB pull-up resistor. This resistor is controlled by USB_SERIAL_JTAG_DP/DM_PULLUP, and the pull-up value is managed by USB_SERIAL_JTAG_PULLUP_VALUE.
  
  - For details on how to configure these settings for different pins (e.g., ESP32-H2 Technical Reference Manual > Chapter [USB Serial/JTAG Controller](#)), see relevant sections in the documentation.

- When the USB function is disabled, USB pins are used as regular GPIOs and the pin’s internal weak pull-up or pull-down resistors can be configured by IO_MUX_GPIOn FUN_WPU/WPD.
  
  - For details on how to configure these settings for different pins (e.g., ESP32-H2 Technical Reference Manual > Chapter [IO MUX and GPIO Matrix](#)), see relevant sections in the documentation.

- Depends on the value of EFUSE_DIS_PAD_JTAG:
  - `0` – WPU is enabled
  - `1` – pin floating

---

**Footer:**

Espressif Systems  
Page number: **14**  
Document title: ESP32-H2 Series Datasheet v1.2  
Link to submit documentation feedback [Submit Documentation Feedback](#)