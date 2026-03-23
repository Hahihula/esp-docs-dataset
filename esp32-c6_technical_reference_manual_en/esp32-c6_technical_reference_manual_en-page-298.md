

```markdown
Register 7.41. LP_IO_STATUS_REG (0x0018)

LP_GPIO_STATUS_INT Configures the interrupt status of GPIO0 ~ GPIO7.
O: No interrupt
1: Interrupt is triggered
Bit0 is corresponding to GPIO0, bit1 is corresponding to GPIO1, and etc. This register is used together with LP_IO_PINn_INT_TYPE in register LP_IO_PINn_REG.
(R/W)

Register 7.42. LP_IO_STATUS_W1TS_REG (0x001C)

LP_GPIO_STATUS_INT_W1TS Configures whether or not to set the interrupt status register LP_IO_STATUS_INT of GPIO0 ~ GPIO7.

- Bit0 is corresponding to GPIO0, bit1 is corresponding to GPIO1, and etc.
- If the value 1 is written to a bit here, the corresponding bit in LP_IO_STATUS_INT will be set to 1.
- Recommended operation: use this register to set LP_IO_STATUS_INT.
(WT)
```