

```markdown
Register 24.4. DS_SET_FINISH_REG (0x0E08)

DS_SET_FINISH Configures whether to end the DSA operation.
O: No effect
1: End the DSA operation
(WO)

Register 24.5. DS_QUERY_BUSY_REG (0x0EOC)

DS_QUERY_BUSY Represents whether the DSA module is idle.
O: The DSA module is idle
1: The DSA module is busy
(RO)

Register 24.6. DS_QUERY_KEY_WRONG_REG (0x0E10)

DS_QUERY_KEY_WRONG Represents the specific problem with HMAC initialization.
O: HMAC is not called
1-15: HMAC was activated, but the DSA peripheral did not successfully receive the DSA_KEY from the HMAC peripheral.
(RO)
```