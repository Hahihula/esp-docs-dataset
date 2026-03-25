

```markdown
- 3 - IE = 1, WPU = 1 (input enabled, pull-up resistor enabled)
- 4 - IE = 1, OE = 1 (input enabled, output enabled)
- 1* - If `EFUSE_DIS_PAD_JTAG` = 1, the pin MTCK is left floating after reset, i.e., IE = 1. If `EFUSE_DIS_PAD_JTAG` = 0, the pin MTCK is connected to internal pull-up resistor, i.e., IE = 1, WPU = 1.
- 3* - IE = 1, WPU = 0. The default value of GPIO14's USB pull-up is 1, which means the pull-up resistor is enabled. For details, please refer to the Notes below.

Notes

R - LP pins. Some LP pins have analog functions. For details, see 6.15-1.
USB - USB pull-up resistor enabled
    - By default, the USB function is enabled for USB pins (i.e., GPIO13 and GPIO14), and the pin pull-up is decided by the USB pull-up. The USB pull-up is controlled by `USB_SERIAL_JTAG_DP/DM_PULLUP` and the pull-up resistor value is controlled by `USB_SERIAL_JTAG_PULLUP_VALUE`. For details, see Chapter USB Serial/JTAG Controller.
    - When the USB function is disabled, USB pins are used as regular GPIOs and the pin's internal weak pull-up and pull-down resistors are disabled by default (configurable by `IO_MUX_GPIOn_MCU_WPU/WPD`).

6.14 LP IO MUX Function List

Table 6.14-1 shows the LP IO MUX functions of each GPIO pin. GPIO pins are default controlled by HP IO MUX. Table 6.14-1 only show the LP IO MUX functions of LP GPIO pins.

Table 6.14-1. LP IO MUX Pin Functions

| GPIO No. | Name          | Function 0 | Function 1 | Function 2 | Function 3 |
|----------|---------------|------------|------------|------------|------------|
| 0        | XTAL_32K_P    | —          | LP_GPIO0   | —          | —          |
| 1        | XTAL_32K_N    | —          | LP_GPIO1   | —          | —          |
| 2        | GPIO2         | —          | LP_GPIO2   | —          | —          |
| 3        | MTMS          | —          | LP_GPIO3   | —          | —          |
| 4        | MTDI          | —          | LP_GPIO4   | —          | —          |
| 5        | MTCK          | —          | LP_GPIO5   | —          | —          |
| 6        | MTDO          | —          | LP_GPIO6   | —          | —          |

Notice:
In LP IO MUX, unused pins must be configured to LP_GPIO function.

6.15 GPIO Pin Analog Function List

Table 6.15-1 shows the GPIO pins and their corresponding analog functions.
```