

```markdown
## 23.7 Registers

The addresses in this section are relative to External Memory Encryption and Decryption base address provided in Table 3.3-3 in Chapter 3 System and Memory.

### Register 23.1. XTS_AES_PLAIN_n_REG (n: 0-15) (0x0000+4*n)

| Bit | Description |
|-----|-------------|
| 31  |             |
|     | 0x000000    |
|     | Reset        |

XTS_AES_PLAIN_n Stores nth 32-bit piece of plain text. (R/W)

### Register 23.2. XTS_AES_LINESIZE_REG (0x0040)

| Bit | Description |
|-----|-------------|
| 31  |             |
|     | 0x00000000  |
|     | Reset        |

XTS_AES_LINESIZE Configures the data size of one encryption operation.
*   0: 16 bytes;
*   1: 32 bytes. (R/W)

### Register 23.3. XTS_AES_DESTINATION_REG (0x0044)

| Bit | Description |
|-----|-------------|
| 31  |             |
|     | 0x00000000  |
|     | Reset        |

XTS_AES_DESTINATION Configures the type of the external memory. Currently, it must be set to 0, as the Manual Encryption block only supports flash encryption. Errors may occur if users write
1.
*   0: flash;
*   1: external RAM. (R/W)
```