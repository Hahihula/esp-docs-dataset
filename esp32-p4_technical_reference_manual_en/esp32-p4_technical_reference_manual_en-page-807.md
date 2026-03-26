

```markdown
Register 12.137. COREO_INTR_SEC_STATUS_REG (0x022C)

COREO_INTR_SEC_STATUS Represents status of the user mode interrupt signals that have been delegated to the machine mode interrupt when COREO is in machine mode. (RO)

Register 12.138. COREO_INTR_SRC_PASS_IN_SEC_STATUS_O_REG (0x0230)

COREO_INTR_SRC_PASS_IN_SEC_STATUS_O Represents whether interrupt source 0 ~ 31 has enabled the interrupt delegation function. Each bit corresponds to the enable status of one interrupt source.

0: Corresponding interrupt source has not enabled the interrupt delegation function.
1: Corresponding interrupt source has enabled the interrupt delegation function.
(RO)
```