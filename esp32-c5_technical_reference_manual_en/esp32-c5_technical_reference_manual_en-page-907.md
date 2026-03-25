

```markdown
Chapter 24 HMAC Accelerator (HMAC)

Register 24.9. HMAC_QUERY_ERROR_REG (0x0068)

HMAC_QUERY_CHECK Represents whether or not an HMAC key matches the purpose.
O: Match
1: Error
(RO)

Register 24.10. HMAC_QUERY_BUSY_REG (0x006C)

HMAC_BUSY_STATE Represents whether or not HMAC is in a busy state. Before configuring HMAC, please make sure HMAC is in an IDLE state.
O: Idle
1: HMAC is still working on the calculation
(RO)

Register 24.11. HMAC_SET_MESSAGE_PAD_REG (0x00F0)

HMAC_SET_TEXT_PAD Configures whether or not the padding is applied by software.
O: Not applied by software
1: Applied by software
(WO)
```