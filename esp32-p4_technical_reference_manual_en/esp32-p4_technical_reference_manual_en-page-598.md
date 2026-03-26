

```markdown
## Register 9.33. GPIO_INTR_3_REG (0x0644)

GPIO_INT_3 Represents the CPU interrupt 3 status of GPIO0 ~ GPIO31. Each bit represents:
- O: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by `GPIO_PINn_INT_TYPE`.
- 1: Represents the GPIO generates an interrupt configured by `GPIO_PINn_INT_TYPE` after the CPU interrupt is enabled.
Bit0 ~ bit31 are corresponding to GPIO0 ~ GPIO31. This interrupt status is corresponding to the bit in `GPIO_STATUS_REG` when assert (high) enable signal (bit17 of `GPIO_PINn_REG`). (RO)

## Register 9.34. GPIO_INTR1_3_REG (0x0648)

GPIO_INT1_3 Represents the CPU interrupt 3 status of GPIO32 ~ GPIO54. Each bit represents:
- O: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by `GPIO_PINn_INT_TYPE`.
- 1: Represents the GPIO generates an interrupt configured by `GPIO_PINn_INT_TYPE` after the CPU interrupt is enabled.
Bit0 ~ bit22 are corresponding to GPIO32 ~ GPIO54. This interrupt status is corresponding to the bit in `GPIO_STATUS1_REG` when assert (high) enable signal (bit17 of `GPIO_PINn_REG`). (RO)

## Register 9.35. GPIO_CLOCK_GATE_REG (0x064C)

GPIO_CLK_EN Configures whether or not to enable clock gate.
- O: Not enable
- 1: Enable, the clock is free running.
(R/W)
```