

```markdown
Register 6.25. IO_MUX_GPIOn_REG (n: 0-13, 22-29) (0x0000+0x4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 18  | IO_MUX_GPIOn_HYS_SEL                                                       |
| 17  | IO_MUX_GPIOn_HYS_EN                                                        |
| 16  | IO_MUX_GPIOn_FILTER_EN                                                     |
| 15  | IO_MUX_GPIOn_MCU_OE                                                         |
| 14  | IO_MUX_GPIOn_FUN_DRV                                                       |
| 13  | IO_MUX_GPIOn_FUN_IE                                                        |
| 12  | IO_MUX_GPIOn_WPU                                                            |
| 11  | IO_MUX_GPIOn_MCU_IE                                                        |
| 10  | IO_MUX_GPIOn_MCU_DRV                                                       |
| 9   | IO_MUX_GPIOn_SLP_SEL                                                      |
| 8   | IO_MUX_GPIOn_MCU_WPDU                                                     |
| 7   | IO_MUX_GPIOn_WPD                                                           |
| 6   | Reset                                                                      |
| 5-0 | 0x1                                                                         |

IO_MUX_GPIOn_MCU_OE Configures whether or not to enable the output of GPIO in sleep mode.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_SLP_SEL Configures whether or not to enter sleep mode for GPIO.
O: Not enter
1: Enter
(R/W)

IO_MUX_GPIOn_MCU_WPD Configure whether or not to enable pull-down resistor of GPIO in sleep mode.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_MCU_WPU Configures whether or not to enable pull-up resistor of GPIO during sleep mode.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_MCU_IE Configures whether or not to enable the input of GPIO during sleep mode.
O: Disable
1: Enable
(R/W)

IO_MUX_GPIOn_MCU_DRV Configures the drive strength of GPIO during sleep mode.
0: ~5 mA
1: ~10 mA
2: ~20 mA
3: ~40 mA
(R/W)

IO_MUX_GPIOn_FUN_WPD Configures whether or not to enable pull-down resistor of GPIO.
O: Disable
1: Enable
(R/W)
```