

```markdown
Chapter 22 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack


Register 22.10. ECDSA_SHA_MODE_REG (0x0200)

| Bit Position | Description         |
|--------------|---------------------|
| 3..0         | ECDSA_SHA_MODE      |

ECDSA_SHA_MODE Configures SHA algorithms for message hash.
1: SHA-224
2: SHA-256
Others: invalid
(R/W)


Register 22.11. ECDSA_SHA_START_REG (0x0210)

| Bit Position | Description         |
|--------------|---------------------|
| 1..0         | ECDSA_SHA_START     |

ECDSA_SHA_START Write 1 to start the first SHA operation in the ECDSA process. This bit will be self-cleared after configuration. (WT)


Register 22.12. ECDSA_SHA_CONTINUE_REG (0x0214)

| Bit Position | Description         |
|--------------|---------------------|
| 1..0         | ECDSA_SHA_CONTINUE   |

ECDSA_SHA_CONTINUE Write 1 to start the latter SHA operation in the ECDSA process. This bit will be self-cleared after configuration. (WT)
```