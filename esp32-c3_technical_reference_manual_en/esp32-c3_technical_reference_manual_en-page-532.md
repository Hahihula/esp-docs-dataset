

```markdown
Register 22.4. DS_SET_FINISH_REG (0x0E08)

DS_SET_FINISH    Write 1 to this register to end DS operation. (WO)


Register 22.5. DS_QUERY_BUSY_REG (0x0EOC)

DS_QUERY_BUSY    1: The DS module is busy; 0: The DS module is idle. (RO)


Register 22.6. DS_QUERY_KEY_WRONG_REG (0x0E10)

DS_QUERY_KEY_WRONG 1-15: HMAC was activated, but the DS peripheral did not successfully receive the DS_KEY from the HMAC peripheral. (The biggest value is 15); 0: HMAC is not called. (RO)
```