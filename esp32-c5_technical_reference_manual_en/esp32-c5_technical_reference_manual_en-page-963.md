

```markdown
Chapter 28 Elliptic Curve Digital Signature Algorithm (ECDSA)    GoBack


Register 28.8. ECDSA_STATE_REG (0x0020)

ECDSA_BUSY Represents the working state of the ECDSA accelerator.
O: IDLE
1: LOAD
2: GAIN
3: BUSY
(RO)


Register 28.9. ECDSA_RESULT_REG (0x0024)

ECDSA_OPERATION_RESULT Indicates if the ECDSA operation is successful.
O: Not successful
1: Successful
Only valid when the ECDSA operation is done.
(RO/SS)
```