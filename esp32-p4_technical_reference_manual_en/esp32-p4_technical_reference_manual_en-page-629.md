

```markdown
Register 9.79. LP_GPIO_FUNCn_OUT_SEL_CFG_REG (n: 0 - 15) (0x00F4+4*n)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31-8      | (reserved)                                                                  |
| 7         | LP_GPIO_FUNCn_OUT_SEL                                                       |
|           |                                                                             |
|           | 6: LP_GPIO_FUNCn_OUT_INV_SEL                                               |
|           | 5: LP_GPIO_FUNCn_OE_INV_SEL                                                |
|           | 4: Reset                                                                    |
|           | 0x20                                                                         |

LP_GPIO_FUNCn_OE_INV_SEL Configures whether or not to invert the output enable signal.
- 0: Not invert
- 1: Invert (R/W)

LP_GPIO_FUNCn_OE_SEL Configures to select the source of output enable signal.
- 0: Use output enable signal from peripheral.
- 1: Force the output enable signal to be sourced from bit n of LP_GPIO_ENABLE_REG. (R/W)

LP_GPIO_FUNCn_OUT_INV_SEL Configures whether or not to invert the output value.
- 0: Not invert
- 1: Invert (R/W)

LP_GPIO_FUNCn_OUT_SEL Configures to select a signal Y (0 <= Y < 32) from 31 peripheral signals to be output to GPIO n.
- 0: Select signal 0
- 1: Select signal 1
- ...
- 30: Select signal 30
- 31: Select signal 31
Or
- 32: Bit n of LP_GPIO_OUT_REG and LP_GPIO_ENABLE_REG are selected as the output value and output enable.

For the detailed signal list, see Table 9.13-1.
(R/W)

9.20.5 LP IO MUX Registers

The addresses in this section are relative to LP IO MUX base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section IX .
```