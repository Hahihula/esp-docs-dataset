

```markdown
Register 6.16. GPIO_FUNCn_OUT_SEL_CFG_REG (n: 0-27) (0x0554+4*n)

| Bit | Description |
|-----|-------------|
| 31  | (reserved) |
| 11  | GPIO_FUNCn_OEN_SEL |
| 10  | GPIO_FUNCn_OEN_INV_SEL |
| 9   | GPIO_FUNCn_OUT_SEL |
| 8   | GPIO_FUNCn_OUT_SEL_CFG_REG (n: 0-27) (0x0554+4*n) |
| 7   | Reset |
| ... |             |
| 3   | 0x80        |

GPIO_FUNCn_OUT_SEL Configures to select a signal Y (0 <= Y < 128) from 128 peripheral signals to be output from GPIO[n].
0: Select signal 0
1: Select signal 1
......
126: Select signal 126
127: Select signal 127
Or
128: Bit n of GPIO_OUT_REG and GPIO_ENABLE_REG are selected as the output value and output enable.

For the detailed signal list, see Table 6.12-1.
(R/W/SC)

GPIO_FUNCn_OUT_INV_SEL Configures whether or not to invert the output value.
0: Not invert
1: Invert
(R/W/SC)

GPIO_FUNCn_OEN_SEL Configures to select the source of output enable signal.
0: Use output enable signal from peripheral.
1: Force the output enable signal to be sourced from bit n of GPIO_ENABLE_REG.
(R/W)

GPIO_FUNCn_OEN_INV_SEL Configures whether or not to invert the output enable signal.
0: Not invert
1: Invert
(R/W)
```