

```markdown
Register 21.12. HMAC_SET_PARA_KEY_REG (0x0048)

HMAC_KEY_SET Configures HMAC key. There are six keys with index 0~5. Write the index of the selected key to this field. (WO)

Register 21.13. HMAC_WR_MESSAGE_n_REG (n: 0-15) (0x0080+4*n)

HMAC_WDATA_n Represents the nth 32-bit of message. (WO)

Register 21.14. HMAC_RD_RESULT_n_REG (n: 0-7) (0x00C0+4*n)

HMAC_RDATA_n Represents the nth 32-bit of hash result. (RO)
```