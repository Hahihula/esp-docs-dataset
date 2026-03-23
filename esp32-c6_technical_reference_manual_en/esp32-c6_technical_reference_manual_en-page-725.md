

```markdown
Chapter 25 External Memory Encryption and Decryption (XTS_AES) GoBack


Register 25.3. XTS_AES_DESTINATION_REG (0x0344)

| 31 | 0 |
|----|---|
|    | Reset |
| 0x00000000 | |

XTS_AES_DESTINATION Configures the type of external memory. Currently, it must be set to 0, as the Manual Encryption block only supports flash encryption. Errors may occur if users write 1.
- O: flash
- 1: external RAM (may cause error)
(R/W)


Register 25.4. XTS_AES_PHYSICAL_ADDRESS_REG (0x0348)

| 31 | 30 | 29 |
|----|----|----|
|    |    | Reset |
| 0x0 | 0x00000000 | |

XTS_AES_PHYSICAL_ADDRESS Configures physical address. Note that its value should be within the range between 0x0000_0000 and 0x00FF_FFFF). (R/W)
```