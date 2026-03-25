

```markdown
Chapter 15 Permission Control (PMS)

Register 15.6. HP_APM_MO_STATUS_REG (0x00C8)

HP_APM_MO_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)

Register 15.7. HP_APM_MO_STATUS_CLR_REG (0x00CC)

HP_APM_MO_REGION_STATUS_CLR Configures to clear exception status. (WT)
```