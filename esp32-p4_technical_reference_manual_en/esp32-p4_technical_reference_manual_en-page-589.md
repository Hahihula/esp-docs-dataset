

```markdown
Register 9.21. GPIO_STATUS1_W1TC_REG (0x0058)

| 31 | 25 | 24 | (reserved) |
|----:|----:|----:|------------|
|    |    |    |            |
| 0x00000 | Reset |

GPIO_STATUS1_W1TC Configures whether or not to clear the interrupt status register GPIO_STATUS1_INTERRUPT of GPIO32 ~ GPIO54.
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54.
If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS1_INTERRUPT will be cleared.

Recommended operation: use this register to clear GPIO_STATUS1_INTERRUPT.
(WT)

Register 9.22. GPIO_INTR_O_REG (0x005C)

| 31 | 0 |
|----|---|
|    |   |
| 0x00000 | Reset |

GPIO_INT_O Represents the CPU interrupt 0 status of GPIO0 ~ GPIO31. Each bit represents:
0: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the CPU interrupt is enabled.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit13 of GPIO_PINn_REG).
(RO)
```