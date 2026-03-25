

```markdown
Register 8.13. GPIO_STATUS_W1TC_REG (0x007C)

| 31 | 0 |
|----|---|
|    |   |
| 0x000000 | Reset |

GPIO_STATUS_W1TC Configures whether or not to clear the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0~GPIO14 and GPIO23~GPIO28.
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.
The value of each bit can be:
O: Not clear
1: The corresponding bit in GPIO_STATUS_INTERRUPT will be cleared.

Recommended operation: use this register to clear GPIO_STATUS_INTERRUPT.
(WT)

Register 8.14. GPIO_STATUS_NEXT_REG (0x00B4)

| 31 | 0 |
|----|---|
|    |   |
| 0x000000 | Reset |

GPIO_STATUS_INTERRUPT_NEXT Represents the interrupt source signal of GPIO0~GPIO14 and GPIO23~GPIO28.
Each bit represents:
O: The GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: The GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE.
The interrupt could be rising edge interrupt, falling edge interrupt, level sensitive interrupt and any edge interrupt.
(RO)
```