

```markdown
Register 8.9. GPIO_PROCPU_INT_REG (0x00A4)

31                                 0
+-----------------------------+
|       0x000000              | Reset
+-----------------------------+

GPIO_PROCPU_INT Represents the CPU interrupt status of GPIO0~GPIO14 and GPIO23~GPIO28.
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.

Each bit represents:
0: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the CPU interrupt is enabled.

This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit13 of GPIO_PINn_REG).
(RO)

Register 8.10. GPIO_SDIO_INT_REG (0x00A8)

31                                 0
+-----------------------------+
|       0x000000              | Reset
+-----------------------------+

GPIO_SDIO_INT Represents the GPIO_SDIO_INT interrupt status of GPIO0~GPIO14 and GPIO23~GPIO28.
Bit[0]~bit[14] and bit[23]~bit[28] are corresponding to GPIO0~GPIO14 and GPIO23~GPIO28.

Each bit represents:
0: Represents GPIO_SDIO_INT interrupt is not enabled, or the GPIO does not generate the interrupt configured by GPIO_PINn_INT_TYPE.
1: Represents the GPIO generates an interrupt configured by GPIO_PINn_INT_TYPE after the GPIO_SDIO_INT interrupt is enabled.

This interrupt status is corresponding to the bit in GPIO_STATUS_REG when assert (high) enable signal (bit15 of GPIO_PINn_REG).
(RO)
```