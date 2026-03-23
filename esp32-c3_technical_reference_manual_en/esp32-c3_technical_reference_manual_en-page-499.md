

```markdown
Register 19.10. HMAC_QUERY_BUSY_REG (0x006C)

HMAC_BUSY_STATE Indicates whether HMAC is in busy state. Before configuring HMAC, please make sure HMAC is in IDLE state. (RO)
- 0: idle.
- 1: HMAC is still working on calculation.

Register 19.11. HMAC_SET_PARA_PURPOSE_REG (0x0044)

HMAC_PURPOSE_SET Determines the HMAC purpose, refer to the Table 19.2-1. (WO)

Register 19.12. HMAC_SET_PARA_KEY_REG (0x0048)

HMAC_KEY_SET Selects HMAC key. There are six keys with index 0~5. Write the index of the selected key to this field. (WO)
```