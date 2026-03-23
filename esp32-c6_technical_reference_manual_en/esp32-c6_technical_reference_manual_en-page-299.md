

```markdown
Register 7.43. LP_IO_STATUS_W1TC_REG (0x0020)

LP_GPIO_STATUS_INT_W1TC Configures whether or not to clear the interrupt status register LP_IO_STATUS_INT of GPIO0 ~ GPIO7.

- Bit0 is corresponding to GPIO00, bit1 is corresponding to GPIO1, and etc.
- If the value 1 is written to a bit here, the corresponding bit in LP_IO_STATUS_INT will be cleared
- recommended operation: use this register to clear LP_IO_STATUS_INT.

(WT)

Register 7.44. LP_IO_IN_REG (0x0024)

LP_GPIO_IN_NEXT Represents the input value of GPIO0 ~ GPIO7.
O: Low level input
1: High level input
bit0 ~ bit7 are corresponding to GPIO0 ~ GPIO7.
(RO)
```