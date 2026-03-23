

```markdown
Register 7.47. LP_IO_STATUS_INT_REG (0x0068)

LP_GPIO_STATUS_INT_NEXT Represents the interrupt source status of GPIO0 ~ GPIO7.
bit0 ~ bit7 are corresponding to GPIO0 ~ 7. Each bit represents:
0: Interrupt source status is invalid.
1: Interrupt source status is valid.

The interrupt here can be rising-edge triggered, falling-edge triggered, any edge triggered, or level triggered.
(RO)

Register 7.48. LP_IO_DATE_REG (0x03FC)

LP_IO_DATE Version control register.
(R/W)
```