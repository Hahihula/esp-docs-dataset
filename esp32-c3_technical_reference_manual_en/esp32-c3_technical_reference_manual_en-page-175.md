

```markdown
- 2 - Drive current = ~20 mA
- 3 - Drive current = ~40 mA


## Reset Configurations

“Reset” column shows the default configuration of each pin after reset:

*   **0** - IE = 0 (input disabled)
*   **1** - IE = 1 (input enabled)
*   **2** - IE = 1, WPD = 1 (input enabled, pull-down resistor enabled)
*   **3** - IE = 1, WPU = 1 (input enabled, pull-up resistor enabled)
*   **4** - OE = 1, WPU = 1 (output enabled, pull-up resistor enabled)
*   **0\*** - IE = 0, WPU = 0. The USB pull-up value of GPIO19 is 1 by default, therefore, the pin’s pull-up resistor is enabled. For more information, see the note below.
*   **1\*** - If eFuse bit `EFUSE_DIS_PAD_JTAG` = 1, the pin MTCK is left floating after reset, i.e. IE = 1. If eFuse bit `EFUSE_DIS_PAD_JTAG` = 0, the pin MTCK is connected to internal pull-up resistor, i.e. IE = 1, WPU = 1.

**Note:**

*   **R** - Pins in VDD3P3_RTC domain, and part of them have analog functions, see Table 5.13-1.
*   **USB** - GPIO18 and GPIO19 are USB pins. The pull-up value of the two pins are controlled by the pins’ pull-up value together with USB pull-up value. If any one of the pull-up value is 1, the pin’s pull-up resistor will be enabled. The pull-up resistors of USB pins are controlled by `USB_SERIAL_JTAG_DP_PULLUP`.
*   **G** - These pins have glitches during power-up. See details in Table 5.12-2.

Table 5.12-2. Power-Up Glitches on Pins

| Pin      | Glitch           | Typical Time Period (ns) |
|----------|------------------|--------------------------|
| MTCK     | Low-level glitch | 5                        |
| MTDO     | Low-level glitch | 5                        |
| GPIO10   | Low-level glitch | 5                        |
| UORXD    | Low-level glitch | 5                        |
| GPIO18   | High-level glitch| 50000                    |

## 5.13 Analog Functions List

Table 5.13-1 shows the IO MUX pins with analog functions.

Table 5.13-1. Analog Functions of IO MUX Pins

| GPIO Num | Pin Name     | Analog Function 0   | Analog Function 1    |
|----------|--------------|--------------------|----------------------|
| 0        | XTAL_32K_P   | XTAL_32K_P         | ADC1_CH0             |
| 1        | XTAL_32K_N   | XTAL_32K_N         | ADC1_CH1             |
| 2        | GPIO2        | -                  | ADC1_CH2             |
```