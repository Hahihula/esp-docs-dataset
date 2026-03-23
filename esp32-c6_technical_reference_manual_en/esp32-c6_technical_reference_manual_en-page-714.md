

```markdown
Register 24.4. DS_SET_FINISH_REG (0x0E08)

DS_SET_FINISH   Configures whether or not to end DS operation.
O: Invalid
1: End DS operation
(WO)


Register 24.5. DS_QUERY_BUSY_REG (0x0EOC)

DS_QUERY_BUSY   Represents whether or not the DS module is idle.
O: The DS module is idle
1: The DS module is busy
(RO)


Register 24.6. DS_QUERY_KEY_WRONG_REG (0x0E10)

DS_QUERY_KEY_WRONG   Represents the specific problem with HMAC initialization.
O: HMAC is not called
1-15: HMAC was activated, but the DS peripheral did not successfully receive the DS_KEY from the HMAC peripheral. (The biggest value is 15)
(RO)
```