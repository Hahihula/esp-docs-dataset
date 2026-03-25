

```markdown
Register 6.13. GPIO_SDIO_INT_REG (0x00A8)

GPIO_SDIO_INT    Represents the GPIO_SDIO_INT interrupt status of GPIO0~GPIO13 and GPIO22~GPIO29.
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
Each bit represents:
0: Represents GPIO_SDIO_INT interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the GPIO_SDIO_INT interrupt is enabled.
This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit[14] of GPIO_PINn_REG).
(RO)

Register 6.14. GPIO_STATUS_NEXT_REG (0x00C4)

GPIO_STATUS_INTERRUPT_NEXT Represents the interrupt source signal of GPIO0~GPIO13 and GPIO22~GPIO29.
Bit[0]~bit[13] and bit[22]~bit[29] are corresponding to GPIO0~GPIO13 and GPIO22~GPIO29.
Each bit represents:
0: The GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: The GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE.
The interrupt could be rising edge interrupt, falling edge interrupt, level sensitive interrupt or any edge interrupt.
(RO)
```