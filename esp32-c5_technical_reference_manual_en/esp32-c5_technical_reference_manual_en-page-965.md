

```markdown
Chapter 28 Elliptic Curve Digital Signature Algorithm (ECDSA) GoBack


Register 28.13. ECDSA_SHA_BUSY_REG (0x0218)

[Diagram: Register layout with bit field labeled "reserved" and single bit at position 0 labeled "ECDSA_SHA_BUSY", reset value shown as 0]

ECDSA_SHA_BUSY Represents the working state of the SHA accelerator in the ECDSA process.
O: IDLE
1: BUSY
(RO)


Register 28.14. ECDSA_DATE_REG (0x00FC)

[Diagram: Register layout with bits 31-28 reserved, bit field at position 27 labeled "ECDSA_DATE", reset value shown as 0x2409180]

ECDSA_DATE The ECDSA version control register. (R/W)
```