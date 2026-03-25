

```markdown
Chapter 23 External Memory Encryption and Decryption (XTS_AES) GoBack


Register 23.3. XTS_AES_DESTINATION_REG (0x0344)

```

| Bit | Description       |
|-----|-------------------|
| 31  | (reserved)        |
| ... |                   |
| 0   | Reset             |

XTS_AES_DESTINATION Configures the type of external memory for Manual Encryption. Currently, it must be set to 0, as the Manual Encryption block only supports flash encryption. Set this bit to 1 may cause an error.
- 0: flash
- 1: external RAM
(R/W)

Register 23.4. XTS_AES_PHYSICAL_ADDRESS_REG (0x0348)

```
| Bit | Description       |
|-----|-------------------|
| 31  | (reserved)        |
| 30  |                   |
| 29  |                   |
| ... |                   |
| 0   | Reset             |

0x000000
```

XTS_AES_PHYSICAL_ADDRESS Configures the physical address which will be used in Manual Encryption. This value should be aligned with the byte number configured via the XTS_AES_LINESIZE parameter. (R/W)
```