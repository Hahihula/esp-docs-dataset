

```markdown
Register 7.20. IO_MUX_GPIOn_REG (n: 0-30) (0x004+4*n)

Continued from the previous page...

IO_MUX_GPIOn_FUN_WPU Configures whether or not enable pull-up resistor of GPIO n.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_FUN_IE Configures whether or not to enable input of GPIO n.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_FUN_DRV Configures the drive strength of GPIO n.
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

Register 7.21. IO_MUX_DATE_REG (0x00FC)
```

```markdown
| 31 | 28 | 27 | ... | 0 |
|----|----|----|-----|---|
| O  | O  | O  |     |   |

IO_MUX_DATE_REG Version control register.
(R/W)
```