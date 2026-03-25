

```markdown
Register 6.11. GPIO_STATUS_W1TC_REG (0x007C)

GPIO_STATUS_W1TC Configures whether or not to clear the interrupt status register GPIO_STATUS_INTERRUPT of GPIO0~GPIO13 and GPIO22~GPIO29.
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
The value of each bit can be:
O: Not clear
1: The corresponding bit in GPIO_STATUS_INTERRUPT will be cleared.

Recommended operation: use this register to clear GPIO_STATUS_INTERRUPT.
(WT)

Register 6.12. GPIO_PROCPU_INT_REG (0x00A4)

GPIO_PROCPU_INT Represents the CPU interrupt status of GPIO0~GPIO13 and GPIO22~GPIO29.
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
Each bit represents:
O: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the CPU interrupt is enabled.
This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit[13] of GPIO_PINn_REG).
(RO)
```