

```markdown
Register 8.58. LP_IO_MUX_GPIOn_REG (n: 0-7) (0x0000+0x4*n)

Continued from the previous page...

LP_IO_MUX_GPIOn_FUN_WPD Configures whether or not to enable the pull-down resistor of GPIO n in normal execution mode.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIOn_FUN_WPU Configures whether or not to enable the pull-up resistor of GPIO n in normal execution mode.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIOn_FUN_IE Configures whether or not to enable the input of GPIO n in normal execution mode.
O: Not enable
1: Enable
(R/W)

LP_IO_MUX_GPIOn_FUN_DRV Configures the drive strength of GPIO n in normal execution mode.
0: ~5 mA
1: ~10 mA
2: ~20 mA
3: ~40 mA
(R/W)

LP_IO_MUX_GPIOn_MCU_SEL Configures to select the LP IO MUX function for GPIO n in normal execution mode.
0: Select Function 0
1: Select Function 1
......

LP_IO_MUX_GPIOn_FILTER_EN Configures whether or not to enable filter for pin input signals.
O: Disable
1: Enable
(R/W)

LP_IO_MUX_GPIOn_HYS_EN Configures whether or not to enable the hysteresis function of the pin when LP_IO_MUX_GPIO n_HYS_SEL is set to 1.
O: Disable
1: Enable
(R/W)

Continued on the next page...
```