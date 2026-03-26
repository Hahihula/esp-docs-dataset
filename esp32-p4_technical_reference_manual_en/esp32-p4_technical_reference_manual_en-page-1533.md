

```markdown
Register 31.9. ECDSA_RESULT_REG (0x0024)

ECDSA_OPERATION_RESULT Indicates if the ECDSA_DS operation is successful.
O: Not successful
1: Successful
Only valid when the ECDSA_DS operation is done.
(RO/SS)
```

```markdown
Register 31.10. ECDSA_SHA_MODE_REG (0x0200)

ECDSA_SHA_MODE Configures SHA algorithms for message hash.
1: SHA-224
2: SHA-256
3: SHA-384
4: SHA-512
5: SHA-512-224
6: SHA-512-256
Others: invalid
(R/W)
```