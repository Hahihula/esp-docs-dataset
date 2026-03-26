

```markdown
Chapter 9 GPIO Matrix and IO MUX



Register 9.25. GPIO_INTR1_1_REG (0x0068)

| 31 | 25 | 24 | ... | 0 |
|----|----|----|-----|---|
| 0  | 0  | 0  | 0   | 0 |

(reserved)
GPIO_INTR1_1

0x00000 Reset



GPIO_INT1_1 Represents the CPU interrupt 1 status of GPIO32 ~ GPIO54. Each bit represents:
O: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the CPU interrupt is enabled.
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. This interrupt status is corresponding to the bit in GPIO_STATUS1_REG when assert (high) enable signal (bit14 of GPIO_PINn_REG).
(RO)



Register 9.26. GPIO_STATUS_NEXT_REG (0x006C)

| 31 | ... | 0 |
|----|-----|---|
|    |     |   |

GPIO_STATUS_INTERRUPT_NEXT

0x000000 Reset



GPIO_STATUS_INTERRUPT_NEXT Represents the interrupt source signal of GPIO0 ~ GPIO31.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. Each bit represents:
O: The GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: The GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE.
The interrupt could be rising edge interrupt, falling edge interrupt, level sensitive interrupt and any edge interrupt.
(RO)
```