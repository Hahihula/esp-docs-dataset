

```markdown
Register 25.9. ECDSA_RESULT_REG (0x0024)

ECDSA_OPERATION_RESULT Indicates if the ECDSA operation is successful.
0: not successful
1: successful
Only valid when the ECDSA operation is done. (RO/SS)

Register 25.10. ECDSA_SHA_MODE_REG (0x0200)

ECDSA_SHA_MODE Configures SHA algorithms for message hash.
1: SHA-224
2: SHA-256
Others: invalid
(R/W)

Register 25.11. ECDSA_SHA_START_REG (0x0210)

ECDSA_SHA_START Write 1 to start the first SHA operation in the ECDSA process. This bit will be self-cleared after configuration. (WT)
```