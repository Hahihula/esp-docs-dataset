

```markdown
## Drive Strength

“DRV” column shows the drive strength of each pin after reset:

*   **0** - Drive current = ~5 mA
*   **1** - Drive current = ~10 mA
*   **2** - Drive current = ~20 mA
*   **3** - Drive current = ~40 mA

## Reset

The default configuration of each pin after reset:

*   **0** - input disabled, in high impedance state (IE = 0)
*   **1** - input enabled, in high impedance state (IE = 1)
*   **1*** - When the value of eFuse bit `FFUSE_DIS_PAD_JTAG` is 0 (default), input enabled, pull-up resistor enabled (IE = 1, WPU = 1)  
    1, input disabled, in high impedance state (IE = 1)
*   **3*** - input disabled, pull-up resistor enabled (IE = 0, USB_PU = 1). See details in Notes.
*   **5** - input disabled (IE = 0). Output is controlled by the peripheral of Function 0, and the default output is 1.

We recommend pulling high or low GPIO pins in high impedance state to avoid unnecessary power consumption. You may add pull-up and pull-down resistors in your PCB design, or enable internal pull-up and pull-down resistors during software initialization.

### Notes

*   **R** - These pins have analog functions.
*   **USB** - The pull-up value of a USB pin is controlled by the pin’s pull-up value together with the USB pull-up value. If any of the two pull-up values is 1, the pin’s pull-up resistor will be enabled.

Notice:
In HP IO MUX, unused pins must be configured to GPIO function.
```

```markdown
## 9.15 LP IO MUX Functions List

Table 9.15-1 shows the LP IO MUX functions of each GPIO pin. GPIO pins are default controlled by HP IO MUX, so Table 9.15-1 only show functions of LP IO MUX.

Table 9.15-1. LP IO MUX Pin Functions

| Name    | Function 0       | Function 1      |
|---------|------------------|-----------------|
| GPIO0   | `LP_GPIO0`       | `LP_GPIO0`      |
| GPIO1   | `LP_GPIO1`       | `LP_GPIO1`      |
| GPIO2   | `LP_GPIO2`       | `LP_GPIO2`      |
```