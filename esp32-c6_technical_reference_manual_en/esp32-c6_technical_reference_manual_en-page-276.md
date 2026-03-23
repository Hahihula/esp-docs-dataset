

```markdown
Register 7.12: GPIO_PCPU_INT_REG (0x005C)
```

| 31 | 0 |
|----|---|
|    |   |
| 0x000000 | Reset |

GPIO_PCPU_INT Represents the CPU interrupt status of GPIO0 ~ GPIO30. Each bit represents:
- 0: Represents CPU interrupt is not enabled, or the GPIO does not generate the interrupt configured by `GPIO_PINn_INT_TYPE`.
- 1: Represents the GPIO generates an interrupt configured by `GPIO_PINn_INT_TYPE` after the CPU interrupt is enabled.

Bit0 ~ bit30 are corresponding to GPIO0 ~ GPIO30. Bit31 is invalid. This interrupt status is corresponding to the bit in `GPIO_STATUS_REG` when assert (high) enable signal (bit13 of `GPIO_PINn_REG`).

(RO)
```