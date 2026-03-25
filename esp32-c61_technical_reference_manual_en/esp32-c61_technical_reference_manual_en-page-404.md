

```markdown
## Register 9.55. INTMTX_COREO_INT_STATUS_2_REG (0x0110)

| 31 | 0 |
|----|---|
| 0x000000 | Reset |

INTMTX_COREO_INT_STATUS_2 Represents the status of the INTMTX sources numbered from 64 ~ 65. Each bit corresponds to one INTMTX source.
- 0: The corresponding INTMTX source triggered an interrupt
- 1: No INTMTX triggered (RO)

## Register 9.56. INTMTX_COREO_SRC_PASS_IN_SEC_STATUS_0_REG (0x0114)

| 31 | 0 |
|----|---|
| 0x000000 | Reset |

INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_0 Represents whether the INTMTX sources numbered from 0 ~ 31 are configured for delegated interrupts. Each bit represents the configuration status of one INTMTX source.
- 0: The corresponding INTMTX source is not configured for delegation.
- 1: The corresponding INTMTX source is configured for delegation. (RO)
```