

```markdown
Chapter 5 IO MUX and GPIO Matrix (GPIO, IO MUX)

Register 5.3. GPIO_OUT_W1TS_REG (0x0008)
| 31 | 26 | 25 | ... | 0 |
|----:|----:|----:|-----|---|
|    |    |    |     | Reset |
| 0  | 0  | 0  | 0   |       |

GPIO_OUT_W1TS GPIO00 ~ 21 output set register. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. If the value 1 is written to a bit here, the corresponding bit in GPIO_OUT_REG will be set to 1. Recommended operation: use this register to set GPIO_OUT_REG. (WT)

Register 5.4. GPIO_OUT_W1TC_REG (0x000C)
| 31 | 26 | 25 | ... | 0 |
|----:|----:|----:|-----|---|
|    |    |    |     | Reset |
| 0  | 0  | 0  | 0   |       |

GPIO_OUT_W1TC GPIO00 ~ 21 output clear register. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. If the value 1 is written to a bit here, the corresponding bit in GPIO_OUT_REG will be cleared. Recommended operation: use this register to clear GPIO_OUT_REG. (WT)

Register 5.5. GPIO_ENABLE_REG (0x0020)
| 31 | 26 | 25 | ... | 0 |
|----:|----:|----:|-----|---|
|    |    |    |     | Reset |
| 0  | 0  | 0  | 0   |       |

GPIO_ENABLE_DATA GPIO output enable register for GPIO0 ~ 21. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. (R/W/SS)
```