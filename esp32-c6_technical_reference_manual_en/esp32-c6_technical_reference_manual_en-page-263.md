

```markdown
- 3 - Drive current = ~40 mA.

## Reset Configurations

“Reset” column shows the default configuration of each pin after reset:

*   0 - IE = 0 (input disabled)
*   1 - IE = 1 (input enabled)
*   2 - IE = 1, WPD = 1 (input enabled, pull-down resistor enabled)
*   3 - IE = 1, WPU = 1 (input enabled, pull-up resistor enabled)
*   4 - OE = 1, WPU = 1 (output enabled, pull-up resistor enabled)
*   **1\*** - If `EFUSE_DIS_PAD_JTAG` = 1, the pin MTCK is left floating after reset, i.e., IE = 1. If `EFUSE_DIS_PAD_JTAG` = 0, the pin MTCK is connected to internal pull-up resistor, i.e., IE = 1, WPU = 1.

**Note:**

*   **R** - Pins in VDDPST1 domain, and part of them have analog functions, see Table 7.13-2.
*   **USB** - GPIO12 and GPIO13 are USB pins. The pull-up value of the two pins are controlled by the pins’ pull-up value together with USB pull-up value. If any one of the pull-up value is 1, the pin’s pull-up resistor will be enabled. The pull-up resistors of USB pins are controlled by `USB_SERIAL_JTAG_DP_PULLUP`.
*   **S0** - For chip variants without an in-package flash, this pin can not be used.
*   **S1** - For chip variants with an in-package flash, this pin can not be used.
*   **S2** - For chip variants with an in-package flash, this pin can only be used to connect the in-package flash, i.e., only Function 0 is available. For chip variants without an in-package flash, this pin can be used as a normal pin, i.e., all the functions are available.

## 7.13 LP IO MUX Functions List

Table 7.13-1 shows the LP GPIO pins and how they correspond to GPIO pins and LP functions.

**Table 7.13-1. LP IO MUX Functions List**

<table><thead><tr><th rowspan="2">LP GPIO No.</th><th rowspan="2">GPIO No.</th><th rowspan="2">GPIO Pin</th><th colspan="2">LP Functions</th></tr><tr><th>0</th><th>1</th></tr></thead><tbody><tr><td>0</td><td>0</td><td>XTAL_32K_P</td><td>LP_GPIO00</td><td>lp_uart_dtrn<sup>1</sup></td></tr><tr><td>1</td><td>1</td><td>XTAL_32K_N</td><td>LP_GPIO1</td><td>lp_uart_dsrn<sup>1</sup></td></tr><tr><td>2</td><td>2</td><td>GPIO2</td><td>LP_GPIO2</td><td>lp_uart_rtsn<sup>1</sup></td></tr><tr><td>3</td><td>3</td><td>GPIO3</td><td>LP_GPIO3</td><td>lp_uart_ctsn<sup>1</sup></td></tr><tr><td>4</td><td>4</td><td>MTMS</td><td>LP_GPIO4</td><td>lp_uart_rxd<sup>1</sup></td></tr><tr><td>5</td><td>5</td><td>MTDI</td><td>LP_GPIO5</td><td>lp_uart_txd<sup>1</sup></td></tr><tr><td>6</td><td>6</td><td>MTCK</td><td>LP_GPIO6</td><td>lp_i2c_sda<sup>2</sup></td></tr><tr><td>7</td><td>7</td><td>MTDO</td><td>LP_GPIO7</td><td>lp_i2c_scl<sup>2</sup></td></tr></tbody></table>
```