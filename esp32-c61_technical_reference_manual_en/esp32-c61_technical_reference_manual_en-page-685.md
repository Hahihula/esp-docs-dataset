

```markdown
Register 16.7. HP_APM_MO_STATUS_CLR_REG (0x00CC)

31 | [reserved] | ... | 1 | 0
   |            |     |    | Reset

HP_APM_MO_EXCEPTION_STATUS_CLR Configures to clear exception status. (WT)


Register 16.8. HP_APM_MO_EXCEPTION_INFO0_REG (0x00D0)

31 | [reserved] | 23 | 22 | 18 | 17 | 16 | 15
   |            |     |     |     |     |     |
   |            | O   | O   | O   | O   | O   | Reset

HP_APM_MO_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_MO_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
HP_APM_MO_EXCEPTION_ID Represents master ID when an exception occurs. (RO)


Register 16.9. HP_APM_MO_EXCEPTION_INFO1_REG (0x00D4)

31 | [reserved] | ... | O
   |            |     | Reset

HP_APM_MO_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```