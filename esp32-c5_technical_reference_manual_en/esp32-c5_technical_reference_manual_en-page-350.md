

```markdown
Register 8.22. GPIO_FUNCn_OUT_SEL_CFG_REG (n: 0-14, 23-28) (0x0AC4+0x4*n)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 12  | GPIO_FUNCn_OE_INV_SEL        |
| 11  | GPIO_FUNCn_OE_SEL            |
| 10  | GPIO_FUNCn_OUT_INV_SEL       |
| 9   | GPIO_FUNCn_OUT_SEL           |
| 8   | GPIO_FUNCn_OUT_SEL_CFG_REG   |
| ... |                              |
| 0   | Reset                        |

GPIO_FUNCn_OUT_SEL Configures to select a signal Y (0 <= Y < 256) from peripheral signals to be output from GPIO[n].
- 0: Select signal 0
- 1: Select signal 1
...
- 254: Select signal 254
- 255: Select signal 255

Or:
- 256: Bit[n] of GPIO_OUT_REG and GPIO_ENABLE_REG are selected as the output value and output enable.

For the detailed signal list, see Table 8.12-1.
(R/W/SC)

GPIO_FUNCn_OUT_INV_SEL Configures whether or not to invert the output value.
- 0: Not invert
- 1: Invert
(R/W/SC)

GPIO_FUNCn_OE_SEL Configures to select the source of output enable signal.
- 0: Use output enable signal from peripheral.
- 1: Force the output enable signal to be sourced from bit[n] of GPIO_ENABLE_REG.
(R/W)

GPIO_FUNCn_OE_INV_SEL Configures whether or not to invert the output enable signal.
- 0: Not invert
- 1: Invert
(R/W)
```