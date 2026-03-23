

```markdown
Chapter 23 External Memory Encryption and Decryption (XTS_AES) GoBack


Register 23.4. XTS_AES_PHYSICAL_ADDRESS_REG (0x0048)

| 31 | 30 | 29 | ... | 0 |
|----:|----:|----:|-----|---|
|   Ox0 |     |     |     | Reset |

XTS_AES_PHYSICAL_ADDRESS Physical address. (Note that its value should be within the range between 0x0000_0000 and 0x00FF_FFFF). (R/W)


Register 23.5. XTS_AES_TRIGGER_REG (0x004C)

| 31 | ... | 1 | 0 |
|----:|-----|---|---|
|     |     | x | Reset |

XTS_AES_TRIGGER Write 1 to enable manual encryption. (WO)


Register 23.6. XTS_AES_RELEASE_REG (0x0050)

| 31 | ... | 1 | 0 |
|----:|-----|---|---|
|     |     | x | Reset |

XTS_AES_RELEASE Write 1 to grant SPI1 access to the encrypted result. (WO)
```