

```markdown
Register 25.12. ECDSA_SHA_CONTINUE_REG (0x0214)

ECDSA_SHA_CONTINUE    Write 1 to start the latter SHA operation in the ECDSA process. This bit will be self-cleared after configuration. (WT)


Register 25.13. ECDSA_SHA_BUSY_REG (0x0218)

ECDSA_SHA_BUSY        Represents the working status of the SHA accelerator in the ECDSA process.
    0: IDLE
    1: BUSY
    (RO)


Register 25.14. ECDSA_DATE_REG (0x00FC)

ECDSA_DATE            The ECDSA version control register. (R/W)
```