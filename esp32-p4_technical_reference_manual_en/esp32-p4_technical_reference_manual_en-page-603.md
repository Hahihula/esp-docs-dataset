

```markdown
Chapter 9 GPIO Matrix and IO MUX

Register 9.43. IO_MUX_GPIOn_REG (n: 0 - 54) (0x0004+4*n)

Continued from the previous page...

IO_MUX_GPIOn_FUN_WPD Configures whether or not to enable pull-down resistor of GPIOn.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_FUN_WPUL Configures whether or not enable pull-up resistor of GPIOn.
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

IO_MUX_GPIOn_MCU_SEL Configures to select IO MUX function for this pin.
O: Select Function 0
1: Select Function 1
......
(R/W)

IO_MUX_GPIOn_FILTER_EN Configures whether or not to enable filter for pin input signals.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 9.44. IO_MUX_DATE_REG (0x0104)

| Bit | Description         |
|-----|---------------------|
| 31  | reserved            |
| 28  |                     |
| 27  |                     |
| ... |                     |
| 0   |                     |

IO_MUX_DATE Version control register.
(R/W)
```

Espressif Systems

603
ESP32-P4 TRM
PRELIMINARY
```