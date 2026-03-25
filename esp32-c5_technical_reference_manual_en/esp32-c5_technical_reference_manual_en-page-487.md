

```markdown
Register 11.76. INTMTX_COREO_SRC_PASS_IN_SEC_STATUS_2_REG (0x0164)

| Bit Range | Description         |
|-----------|---------------------|
| 31        | (reserved)          |
| 20-19     |                     |
|           | 0x000               |
|           | Reset               |

INTMTX_COREO_INT_SRC_PASS_IN_SEC_STATUS_2 Represents whether the INTMTX sources numbered from 64 ~ 83 are configured for delegated interrupts. Each bit represents the configuration status of one INTMTX source.
- 0: The corresponding INTMTX source is not configured for delegation.
- 1: The corresponding INTMTX source is configured for delegation.
(RO)

Register 11.77. INTMTX_COREO_INT_SIG_IDX_ASSERT_IN_SEC_REG (0x0168)

| Bit Range | Description         |
|-----------|---------------------|
| 31        | (reserved)          |
| 6-5       |                     |
|           | 0x0                 |
|           | Reset               |

INTMTX_COREO_INT_SIG_IDX_ASSERT_IN_SEC Configure which CPU Machine Mode INTMTX source the interrupt should be delegated to. (R/W)
```