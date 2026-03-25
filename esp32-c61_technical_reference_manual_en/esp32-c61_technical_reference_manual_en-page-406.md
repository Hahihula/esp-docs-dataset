

```markdown
## Register 9.59. INTMTX_COREO_INT_SIG_IDX_ASSERT_IN_SEC_REG (0x0120)

| Bit 31 | ... | 6 | 5 | 0 |
|--------|-----|---|---|---|
|        |     |   |   | `0x0` Reset |

INTMTX_COREO_INT_SIG_IDX_ASSERT_IN_SEC Configure which CPU Machine Mode INTMTX source the interrupt should be delegated to. (R/W)

## Register 9.60. INTMTX_COREO_SECURE_STATUS_REG (0x0124)

| Bit 31 | ... | 0 |
|--------|-----|---|
|        |     | `0x000000` Reset |

INTMTX_COREO_INT_SECURE_STATUS Represents which CPU User Mode interrupt the delegated Machine Mode interrupt was originally mapped to. (RO)

## Register 9.61. INTMTX_COREO_CLOCK_GATE_REG (0x0128)

| Bit 31 | ... | 1 | 0 |
|--------|-----|---|---|
|        |     |   | `0` Reset |

INTMTX_COREO_REG_CLK_EN INTMTX clock gating configure register. (R/W)
```