

```markdown
Register 21.9. HMAC_QUERY_ERROR_REG (0x0068)

HMAC_QUERY_CHECK Represents whether an HMAC key matches the purpose.
O: Match
1: Error
(RO)
```

```markdown
Register 21.10. HMAC_QUERY_BUSY_REG (0x006C)

HMAC_BUSY_STATE Represents whether HMAC is in a busy state. Before configuring HMAC, please make sure HMAC is in IDLE state.
O: Idle
1: HMAC is still working on calculation
(RO)
```

```markdown
Register 21.11. HMAC_SET_PARA_PURPOSE_REG (0x0044)

HMAC_PURPOSE_SET Configures the HMAC purpose, refer to the Table 21.2-1. (WO)
```