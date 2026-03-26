

```markdown
Chapter 31 ECDSA Digital Signature Peripheral (ECDSA_DS)
GoBack

Register 31.11. ECDSA_SHA_START_REG (0x0210)

[Diagram: Register layout with bit field from 31 to 0, labeled "reserved" for most bits, and a single bit at position 0 labeled "Reset". The bit is named "ECDSA_SHA_START".]

ECDSA_SHA_START Write 1 to start the first SHA operation in the ECDSA_DS process. This bit will be self-cleared after configuration. (WT)

Register 31.12. ECDSA_SHA_CONTINUE_REG (0x0214)

[Diagram: Register layout with bit field from 31 to 0, labeled "reserved" for most bits, and a single bit at position 0 labeled "Reset". The bit is named "ECDSA_SHA_CONTINUE".]

ECDSA_SHA_CONTINUE Write 1 to start the latter SHA operation in the ECDSA_DS process. This bit will be self-cleared after configuration. (WT)

Register 31.13. ECDSA_SHA_BUSY_REG (0x0218)

[Diagram: Register layout with bit field from 31 to 0, labeled "reserved" for most bits, and a single bit at position 0 labeled "Reset". The bit is named "ECDSA_SHA_BUSY".]

ECDSA_SHA_BUSY Represents the working state of the SHA accelerator in the ECDSA_DS process.
0: IDLE
1: BUSY
(RO)
```