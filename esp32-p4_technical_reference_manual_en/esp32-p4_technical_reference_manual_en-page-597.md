

```markdown
Register 9.31. GPIO_INTR_2_REG (0x063C)

GPIO_INT_2 Represents the CPU interrupt 2 status of GPIO0 ~ GPIO31. Each bit represents:
O: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the CPU interrupt is enabled.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit16 of GPIO_PINn_REG).
(RO)

Register 9.32. GPIO_INTR1_2_REG (0x0640)

GPIO_INT1_2 Represents the CPU interrupt 2 status of GPIO32 ~ GPIO54. Each bit represents:
O: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the CPU interrupt is enabled.
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. This interrupt status is corresponding to the bit in GPIO_STATUS1_REG when assert (high) enable signal (bit16 of GPIO_PINn_REG).
(RO)
```