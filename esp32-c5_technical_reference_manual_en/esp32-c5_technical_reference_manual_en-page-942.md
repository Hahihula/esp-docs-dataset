

```markdown
Register 27.4. DS_QUERY_BUSY_REG (0x0E0C)

DS_QUERY_BUSY Represents whether or not the DSA module is idle.
O: The DSA module is idle
1: The DSA module is busy
(RO)
```

```markdown
Register 27.5. DS_QUERY_KEY_WRONG_REG (0x0E10)

DS_QUERY_KEY_WRONG Represents the specific problem with HMAC initialization.
O: HMAC is not called
1-15: HMAC was activated, but the DSA peripheral did not successfully receive the DSA_KEY from the HMAC peripheral.
Larger than 15: invalid
(RO)
```