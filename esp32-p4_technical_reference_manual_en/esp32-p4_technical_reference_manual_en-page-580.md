

```markdown
Register 9.3. GPIO_OUT_W1TC_REG (0x000C)

| 31 | 0 |
|----|---|
|    |   |
| 0x000000 | Reset |

GPIO_OUT_W1TC Configures whether or not to clear the output register `GPIO_OUT_REG` of GPIO0 ~ GPIO31 output.
O: Not clear
1: The corresponding bit in `GPIO_OUT_REG` will be cleared.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. Recommended operation: use this register to clear `GPIO_OUT_REG`.
(WT)

Register 9.4. GPIO_OUT1_REG (0x0010)

| 31 | 25 | 24 | ... | 0 |
|----|----|----|-----|---|
|    |    |    |     |   |
| 0x00000 | Reset |

GPIO_OUT1_DATA_ORIG Configures the output value of GPIO32 ~ GPIO54 output in simple GPIO output mode.
O: Low level
1: High level
The value of bit0 ~ bit22 correspond to the output value of GPIO32 ~ GPIO54 respectively.
(R/W/SC/WTC)
```