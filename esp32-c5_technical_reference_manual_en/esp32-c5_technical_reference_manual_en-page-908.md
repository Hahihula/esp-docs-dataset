

```markdown
Register 24.12. HMAC_ONE_BLOCK_REG (0x00F4)

HMAC_SET_ONE_BLOCK    Write 1 to indicate there is only one block which already contains padding bits and there is no need for padding. (WS)

Register 24.13. HMAC_SET_PARA_PURPOSE_REG (0x0044)

HMAC_PURPOSE_SET      Configures the HMAC purpose, refer to the Table <a href="tab:hmac-key-purpose">link</a>. " (WO)

Register 24.14. HMAC_SET_PARA_KEY_REG (0x0048)

HMAC_KEY_SET          Configures HMAC key. There are six eFuse keys with index 0 verb+ + 5 and one key from the key manager with index 7. Write the index of the selected key to this field. (WO)
```