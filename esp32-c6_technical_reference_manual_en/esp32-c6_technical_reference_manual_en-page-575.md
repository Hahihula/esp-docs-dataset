

```markdown
Register 16.6. HP_APM_MO_STATUS_REG (0x00C8)

HP_APM_MO_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents authority_exception
bit1: 1 represents space_exception
(RO)


Register 16.7. HP_APM_MO_STATUS_CLR_REG (0x00CC)

HP_APM_MO_REGION_STATUS_CLR Configures to clear exception status. (WT)


Register 16.8. HP_APM_MO_EXCEPTION_INFOO_REG (0x00DO)
```

```markdown
HP_APM_MO_EXCEPTION_REGION Represents exception region. (RO)
HP_APM_MO_EXCEPTION_MODE Represents exception mode. (RO)
HP_APM_MO_EXCEPTION_ID Represents exception id information. (RO)
```