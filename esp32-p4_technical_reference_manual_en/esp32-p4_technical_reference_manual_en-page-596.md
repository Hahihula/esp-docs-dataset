

```markdown
Register 9.30. GPIO_FUNCn_OUT_SEL_CFG_REG (n: 0 - 54) (0x0558+0x4*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| ... |                                                                             |
| 12  | GPIO_FUNCn_OE_INV_SEL                                                      |
| 11  | GPIO_FUNCn_OE_SEL                                                           |
| 10  | GPIO_FUNCn_OUT_SEL                                                          |
| 9   | GPIO_FUNCn_OUT_SEL                                                          |
| 8   | GPIO_FUNCn_OUT_SEL                                                          |
| ... |                                                                             |
| 0   | Reset                                                                       |

GPIO_FUNCn_OUT_SEL Configures to select a signal Y (0 <= Y < 256) from 256 peripheral signals to be output to GPIO[n].
0: Select signal 0
1: Select signal 1

......

254: Select signal 254
255: Select signal 255

Or

256: Bitn of GPIO_OUT_REG and GPIO_OUT1_REG are selected as the output value, GPIO_ENABLE_REG and GPIO_ENABLE1_REG are selected as the output enable.
257 ~ 511: invalid

For the detailed signal list, see Table 9.12-1.

(R/W/SC)

GPIO_FUNCn_OUT_INV_SEL Configures whether or not to invert the output value.
0: Not invert
1: Invert
(R/W/SC)

GPIO_FUNCn_OE_SEL Configures to select the source of output enable signal.
0: Use output enable signal from peripheral.
1: Force the output enable signal to be sourced from bitn (n: 0 ~ 31) of GPIO_ENABLE_REG and bitn-32 (n: 32 ~ 54) of GPIO_ENABLE1_REG.

(R/W)

GPIO_FUNCn_OE_INV_SEL Configures whether or not to invert the output enable signal.
0: Not invert
1: Invert

(R/W)
```