

```markdown
Register 6.11. GPIO_STATUS_W1TC_REG (0x004C)

GPIO_STATUS_W1TC Configures whether or not to clear the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0 ~ GPIO27.

- bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid.
- If the value 1 is written to a bit here, the corresponding bit in GPIO_STATUS_INTERRUPT will be cleared.
- Recommended operation: use this register to clear GPIO_STATUS_INTERRUPT.

(WT)

Register 6.12. GPIO_PCPU_INT_REG (0x005C)

GPIO_PROCPU_INT Represents the CPU interrupt status of GPIO0 ~ GPIO27.

- bit0 ~ bit27 are corresponding to GPIO0 ~ GPIO27. Bit28 ~ bit31 are invalid.
- This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit13 of GPIO_PINn_REG). Each bit represents:
  - 0: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
  - 1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the CPU interrupt is enabled.

(RO)
```