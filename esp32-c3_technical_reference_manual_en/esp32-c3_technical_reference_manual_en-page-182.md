

```markdown
Chapter 5 IO MUX and GPIO Matrix (GPIO, IO MUX)
Register 5.9. GPIO_IN_REG (0x003C)

reserved
GPIO_IN_DATA_NEXT

| 31 | 26 | 25 | ... | 0 |
|-----|----|----|-----|---|
| 0   | 0  | 0  | 0   | 0 |
|     |     |     |      | Reset |

GPIO_IN_DATA_NEXT GPIO0 ~ 21 input value. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. Each bit represents a pin input value, 1 for high level and 0 for low level. (RO)

Register 5.10. GPIO_STATUS_REG (0x0044)

reserved
GPIO_STATUS_INTERRUPT

| 31 | 26 | 25 | ... | 0 |
|-----|----|----|-----|---|
| 0   | 0  | 0  | 0   | 0 |
|     |     |     |      | Reset |

GPIO_STATUS_INTERRUPT GPIO0 ~ 21 interrupt status register. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. (R/W/SS)

Register 5.11. GPIO_STATUS_W1TS_REG (0x0048)

reserved
GPIO_STATUS_W1TS

| 31 | 26 | 25 | ... | 0 |
|-----|----|----|-----|---|
| 0   | 0  | 0  | 0   | 0 |
|     |     |     |      | Reset |

GPIO_STATUS_W1TS GPIO0 ~ 21 interrupt status set register. Bit0 ~ bit21 are corresponding to GPIO0 ~ 21, and bit22 ~ bit25 are invalid. If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be set to 1. Recommended operation: use this register to set GPIO_STATUS_INTERRUPT. (WT)
```