

```markdown
## Drive Strength

“DRV” column shows the drive strength of each pin after reset:

*   **0** - Drive current = ~5 mA
*   **1** - Drive current = ~10 mA
*   **2** - Drive current = ~20 mA
*   **3** - Drive current = ~40 mA

## Reset

The default configuration of each pin after reset:

*   **0** - IE = 0 (input disabled)
*   **1** - IE = 1 (input enabled)
*   **3** - IF = 1, WPU = 1 (input enabled, pull-up resistor enabled)
*   **4** - IE = 1, OE = 1 (input enabled, output enabled)
*   **1*** - If `EFUSE_DIS_PAD_JTAG` = 1, the pin MTCK is left floating after reset, i.e., IE = 1. If `EFUSE_DIS_PAD_JTAG` = 0, the pin MTCK is connected to internal pull-up resistor, i.e., IE = 1, WPU = 1.
*   **3*** - IE = 1, WPU = 0. The default value of GPIO14’s USB pull-up is 1, which means the pull-up resistor is enabled. For details, please refer to the [Notes](#notes) below.

## Notes

*   **R** - LP pins. Some LP pins have analog functions. For details, see [8.15-1](#).
*   **USB** - USB pull-up resistor enabled
    *   By default, the USB function is enabled for USB pins (i.e., GPIO13 and GPIO14), and the pin pull-up is decided by the USB pull-up. The USB pull-up is controlled by `USB_SERIAL_JTAG_DP/DM_PULLUP` and the pull-up resistor value is controlled by `USB_SERIAL_JTAG_PULLUP_VALUE`. For details, see [ESP32-C5 Technical Reference Manual](#) > Chapter USB Serial/JTAG Controller.
    *   When the USB function is disabled, USB pins are used as regular GPIOs and the pin’s internal weak pull-up and pull-down resistors are disabled by default (configurable by `IO_MUX_GPIOx_MCU_WPU/WPD`).

## 8.14 LP IO MUX Function List

Table [8.14-1](#) shows the LP IO MUX functions of each GPIO pin. GPIO pins are default controlled by HP IO MUX, so Table [8.14-1](#) only show functions of LP IO MUX.

**Table 8.14-1. LP IO MUX Pin Functions**

| LP IO Name | Function 0          | Function 1*         | Function 2 | Function 3 |
|------------|---------------------|---------------------|----------|----------|
| GPIOO      | LP_UART_DTRN        | LP_GPIOO            | —        | —        |
| GPIO1      | LP_UART_DSRN        | LP_GPIO1            | —        | —        |
| GPIO2      | LP_UART_RTSN        | LP_GPIO2            | —        | LP_I2C_SDA |
| GPIO3      | LP_UART_CTSN        | LP_GPIO3            | —        | LP_I2C_SCL |
```