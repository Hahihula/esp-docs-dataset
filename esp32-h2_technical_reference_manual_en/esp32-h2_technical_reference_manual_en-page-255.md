

```markdown
Register 6.20. IO_MUX_GPIOn_REG (n: 0-27) (0x0004+4*n)

Continued from the previous page...

IO_MUX_GPIOn_FUN_WPU Configures whether or not enable pull-up resistor of GPIOn.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_FUN_IE Configures whether or not to enable input of GPIOn.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_FUN_DRV Configures the drive strength of GPIOn.
O: ~5 mA
1: ~10 mA
2: ~20 mA
3: ~40 mA
(R/W)

IO_MUX_GPIOn_MCU_SEL Configures to select IO MUX function for this signal.
O: Select Function 0
1: Select Function 1
......
(R/W)

IO_MUX_GPIOn_FILTER_EN Configures whether or not to enable filter for pin input signals.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_HYS_EN Configures whether or not to enable the hysteresis function of the pin when IO_MUX_GPIOn_HYS_SEL is set to 1.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_HYS_SEL Configures to choose the signal for enabling the hysteresis function for GPIOn.
OOChoose the output enable signal of eFuse
1: Choose the output enable signal of IO_MUX_GPIOn_HYS_EN.
(R/W)
```