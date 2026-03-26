

```markdown
Register 9.23. GPIO_INTR1_O_REG (0x0060)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | 0: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by `GPIO_PINn_INT_TYPE`. <br> 1: Represents the GPIO generates an interrupt configured by `GPIO_PINn_INT_TYPE` after the CPU interrupt is enabled. <br> Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. This interrupt status is corresponding to the bit in `GPIO_STATUS1_REG` when assert (high) enable signal (bit13 of `GPIO_PINn_REG`). (RO) |

Register 9.24. GPIO_INTR1_REG (0x0064)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | 0: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by `GPIO_PINn_INT_TYPE`. <br> 1: Represents the GPIO generates an interrupt configured by `GPIO_PINn_INT_TYPE` after the CPU interrupt is enabled. <br> Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. This interrupt status is corresponding to the bit in `GPIO_STATUS_REG` when assert (high) enable signal (bit14 of `GPIO_PINn_REG`). (RO) |
```