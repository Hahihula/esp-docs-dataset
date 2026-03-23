

```markdown
Register 10.60. INTMTX_COREO_INT_STATUS_O_REG (0x0134)

| 31 | 0 |
|-----|----|
|     |    |
| 0x000000 | Reset |

INTMTX_COREO_INT_STATUS_O Represents the status of the interrupt sources numbered from 0 ~ 31. Each bit corresponds to one interrupt source.
- 0: The corresponding interrupt source triggered an interrupt
- 1: No interrupt triggered (RO)

Register 10.61. INTMTX_COREO_INT_STATUS_1_REG (0x0138)

| 31 | 0 |
|-----|----|
|     |    |
| 0x000000 | Reset |

INTMTX_COREO_INT_STATUS_1 Represents the status of the interrupt sources numbered from 32 ~ 63. Each bit corresponds to one interrupt source.
- 0: The corresponding interrupt source triggered an interrupt
- 1: No interrupt triggered (RO)
```