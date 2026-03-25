

```markdown
Register 8.53. LP_GPIO_STATUS_NEXT_REG (0x002C)
```

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 8   | LP_GPIO_STATUS_INTERRUPT_NEXT                                               |
| 7~0 | Reset                                                                       |

LP_GPIO_STATUS_INTERRUPT_NEXT Represents the interrupt source status of GPIO0~GPIO6.

Bit[0]~bit[6] are corresponding to GPIO0~GPIO6.

Each bit represents:

0: Interrupt source status is invalid.

1: Interrupt source status is valid.

The interrupt here can be rising-edge triggered, falling-edge triggered, any edge triggered, or level triggered.

(RO)
```