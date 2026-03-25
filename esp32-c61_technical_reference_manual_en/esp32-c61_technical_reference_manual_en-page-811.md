

```markdown
Register 22.8. ECDSA_STATE_REG (0x0020)

ECDSA_BUSY Represents the working state of the ECDSA accelerator.
O: IDLE
1: LOAD
2: GAIN
3: BUSY
(RO)
```

```markdown
Register 22.9. ECDSA_RESULT_REG (0x0024)

ECDSA_OPERATION_RESULT Indicates if the ECDSA operation is successful.
O: Not successful
1: Successful
Only valid when the ECDSA operation is done.
(RO/SS)

ECDSA_K_VALUE_WARNING Indicates if the k value is greater than the base point order.
O: k value is not greater than the base point order. In this case, the k value is the set k value.
1: k value is greater than the base point order. In this case, the k value is the set k mod n.
Only valid when the ECDSA operation is done. (RO/SS)
```