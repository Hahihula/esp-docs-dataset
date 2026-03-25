

```markdown
Chapter 26 External Memory Encryption and Decryption (XTS_AES) GoBack


Register 26.8. XTS_AES_RELEASE_REG (0x0350)

| 31 | 0x00000000 | Reset |
|----|------------|-------|
|    |            |       |

XTS_AES_RELEASE Configures whether to grant SPI1 access to the encrypted result.
O: No effect
1: Grant SPI1 access (WO)


Register 26.9. XTS_AES_DESTROY_REG (0x0354)

| 31 | 0x00000000 | Reset |
|----|------------|-------|
|    |            |       |

XTS_AES_DESTROY Configures whether to destroy the encrypted result.
O: No effect
1: Destroy encrypted result (WO)


Register 26.10. XTS_AES_STATE_REG (0x0358)

| 31 | 0x00000000 | Reset |
|----|------------|-------|
|    |            |       |

XTS_AES_STATE Represents the status of the Manual Encryption block.
O (XTS_AES_IDLE): Idle
1 (XTS_AES_BUSY): Busy with encryption
2 (XTS_AES_DONE): Encryption completed, but the encrypted result is not accessible to SPI
3 (XTS_AES_RELEASE): Encrypted result is accessible to SPI (RO)
```