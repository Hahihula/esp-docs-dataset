

```markdown
Register 9.27. GPIO_STATUS_NEXT1_REG (0x0070)

| Bit | Description         |
|-----|---------------------|
| 31  | (reserved)          |
| 30  |                     |
| 25  |                     |
| 24  |                     |
|     |                     |
| 0   |                     |

GPIO_STATUS_INTERRUPT_NEXT1 Represents the interrupt source signal of GPIO32 ~ GPIO54.
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. Each bit represents:
O: The GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: The GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE.
The interrupt could be rising edge interrupt, falling edge interrupt, level sensitive interrupt and any edge interrupt.
(RO)
```