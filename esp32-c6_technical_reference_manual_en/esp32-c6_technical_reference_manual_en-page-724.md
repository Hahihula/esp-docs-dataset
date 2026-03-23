

```markdown
## 25.8 Registers

The addresses in this section are relative to External Memory Encryption and Decryption base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 25.1. XTS_AES_PLAIN_n_REG (n: 0-15) (0x0300+4*n)

| Bit | Description |
|-----|-------------|
| 31  | 0           |
|     |             |
|     | 0x000000    | Reset |

XTS_AES_PLAIN_n Configures the nth 32-bit piece of plain text. (R/W)

### Register 25.2. XTS_AES_LINESIZE_REG (0x0340)

| Bit | Description |
|-----|-------------|
| 32  |             |
|     |             |
|     | 0x00000000  | Reset |

XTS_AES_LINESIZE Configures the data size of one encryption operation.
- 0: 16 bytes
- 1: 32 bytes
- 2: 64 bytes
- 3: Invalid

(R/W)
```