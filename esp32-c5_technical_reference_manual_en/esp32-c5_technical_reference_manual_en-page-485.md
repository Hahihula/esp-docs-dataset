

```markdown
Register 11.72. INTMTX_COREO_INT_STATUS_1_REG (0x0154)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | 0                                                                             |
|     | Reset                                                                        |

INTMTX_COREO_INT_STATUS_1 Represents the status of the INTMTX sources numbered from 32 ~ 63. Each bit corresponds to one INTMTX source.
- 0: No interrupt triggered from the corresponding INTMTX source
- 1: The corresponding INTMTX source triggered an interrupt (RO)

Register 11.73. INTMTX_COREO_INT_STATUS_2_REG (0x0158)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
|     | 0                                                                             |
| 20  | 19                                                                          |
|     | 0x000000                                                                    |

INTMTX_COREO_INT_STATUS_2 Represents the status of the INTMTX sources numbered from 64 ~ 83. Each bit corresponds to one INTMTX source.
- 0: No interrupt triggered from the corresponding INTMTX source
- 1: The corresponding INTMTX source triggered an interrupt (RO)
```