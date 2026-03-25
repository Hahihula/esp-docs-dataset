

```markdown
Register 28.10. ECDSA_SHA_MODE_REG (0x0200)

| Bit Range | Description         |
|-----------|---------------------|
| 31-4      | (reserved)          |
| 3         | ECDSA_SHA_MODE      |
| 0         | Reset               |

ECDSA_SHA_MODE Configures SHA algorithms for message hash.
1: SHA-224
2: SHA-256
3: SHA-384
4: SHA-512
5: SHA-512-224
6: SHA-512-256
Others: invalid
(R/W)

Register 28.11. ECDSA_SHA_START_REG (0x0210)

| Bit Range | Description         |
|-----------|---------------------|
| 31        | (reserved)          |
| 1         | ECDSA_SHA_START     |
| 0         | Reset               |

ECDSA_SHA_START Write 1 to start the first SHA operation in the ECDSA process. This bit will be self-cleared after configuration. (WT)

Register 28.12. ECDSA_SHA_CONTINUE_REG (0x0214)

| Bit Range | Description         |
|-----------|---------------------|
| 31        | (reserved)          |
| 1         | ECDSA_SHA_CONTINUE  |
| 0         | Reset               |

ECDSA_SHA_CONTINUE Write 1 to start the latter SHA operation in the ECDSA process. This bit will be self-cleared after configuration. (WT)
```