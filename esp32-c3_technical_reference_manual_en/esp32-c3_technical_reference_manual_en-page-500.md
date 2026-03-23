

```markdown
Register 19.13. HMAC_WR_MESSAGE_n_REG (n: 0-15) (0x0080+4*n)

HMAC_WDATA_n Store the nth 32-bit of message. (WO)


Register 19.14. HMAC_RD_RESULT_n_REG (n: 0-7) (0x00C0+4*n)

HMAC_RDATA_n Read the nth 32-bit of hash result. (RO)


Register 19.15. HMAC_SET_MESSAGE_PAD_REG (0x00F0)

HMAC_SET_TEXT_PAD Set this bit to indicate that padding is applied by software. (WO)


Register 19.16. HMAC_ONE_BLOCK_REG (0x00F4)

HMAC_SET_ONE_BLOCK Set this bit when there is only one block which already contains padding bits. (WO)
```