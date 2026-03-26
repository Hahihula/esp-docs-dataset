

```markdown
Register 30.4. DSA_SET_FINISH_REG (0x0E08)

DSA_SET_FINISH Configures whether to end the RSA_DS operation.
O: No effect
1: End the RSA_DS operation
(WO)

Register 30.5. DSA_QUERY_BUSY_REG (0x0EOC)

DSA_QUERY_BUSY Represents whether the RSA_DS peripheral is idle.
O: The RSA_DS peripheral is idle.
1: The RSA_DS peripheral is busy.
(RO)

Register 30.6. DSA_QUERY_KEY_WRONG_REG (0x0E10)

DSA_QUERY_KEY_WRONG Represents the specific problem with HMAC initialization.
O: HMAC is not called.
1-15: HMAC was activated, but the RSA_DS peripheral did not successfully receive
RSA_DS_KEY from the HMAC peripheral.
(RO)
```