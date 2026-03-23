

```markdown
Register 5.16. GPIO_FUNCn_IN_SEL_CFG_REG (n: 0-127) (0x0154+4*n)

| 31 | 30 | 29 | 28 | ... | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|----:|-----|---:|---:|---:|---:|---:|---:|---:|---:|---:|
|    |    |    |    | (reserved) |   |   | GPIO_SIGn_IN_SEL | GPIO_FUNCn_IN_INV_SEL | GPIO_FUNCn_IN_SEL | Reset |
| 0 | 0 | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 |

GPIO_FUNCn_IN_SEL Selection control for peripheral input signal n, selects a pin from the 22 GPIO matrix pins to connect this input signal. Or selects 0x1e for a constantly high input or 0x1f for a constantly low input. (R/W)

GPIO_FUNCn_IN_INV_SEL Invert the input value. 1: invert enabled; 0: invert disabled. (R/W)

GPIO_SIGn_IN_SEL Bypass GPIO matrix. 1: route signals via GPIO matrix; 0: connect signals directly to peripheral configured in IO MUX. (R/W)


Register 5.17. GPIO_FUNCn_OUT_SEL_CFG_REG (n: 0-21) (0x0554+4*n)

| 31 | 30 | 29 | 28 | ... | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----:|----:|----:|----:|-----|----:|----:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
|    |    |    |    | (reserved) | GPIO_FUNCn_OEN_INV_SEL | GPIO_FUNCn_OEN_SEL | GPIO_FUNCn_OEN_SEL | GPIO_FUNCn_OUT_INV_SEL | GPIO_FUNCn_OUT_SEL | Reset |
| 0 | 0 | ... | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x80 |

GPIO_FUNCn_OUT_SEL Selection control for GPIO output n. If a value Y (0<=Y<128) is written to this field, the peripheral output signal Y will be connected to GPIO output n. If a value 128 is written to this field, bit n of GPIO_OUT_REG and GPIO_ENABLE_REG will be selected as the output value and output enable. (R/W)

GPIO_FUNCn_OUT_INV_SEL 0: Do not invert the output value; 1: Invert the output value. (R/W)

GPIO_FUNCn_OEN_SEL 0: Use output enable signal from peripheral; 1: Force the output enable signal to be sourced from bit n of GPIO_ENABLE_REG. (R/W)

GPIO_FUNCn_OEN_INV_SEL 0: Do not invert the output enable signal; 1: Invert the output enable signal. (R/W)
```