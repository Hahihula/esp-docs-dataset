

```markdown
## Register 27.8. HMAC_SET_INVALIDATE_DS_REG (0x0064)

| Bit 31 | 30-0 | Description |
|--------|-------|-------------|
|       |      | Reset       |
|        |      |             |

HMAC_SET_INVALIDATE_DS Configures whether or not to clear calculation results of the RSA_DS peripheral in downstream mode.
O: Not clear
1: Clear calculation results
(WO)

## Register 27.9. HMAC_QUERY_ERROR_REG (0x0068)

| Bit 31 | 30-0 | Description |
|--------|-------|-------------|
|       |      | Reset       |
|        |      |             |

HMAC_QUERY_CHECK Represents whether or not an HMAC key matches the purpose.
O: Match
1: Error
(RO)

## Register 27.10. HMAC_QUERY_BUSY_REG (0x006C)

| Bit 31 | 30-0 | Description |
|--------|-------|-------------|
|       |      | Reset       |
|        |      |             |

HMAC_BUSY_STATE Represents whether or not HMAC is in a busy state. Before configuring HMAC, please make sure HMAC is in an IDLE state.
O: Idle
1: HMAC is still working on the calculation
(RO)
```