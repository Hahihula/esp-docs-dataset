

```markdown
Register 16.16. HP_APM_M2_EXCEPTION_INFO0_REG (0x00F0)

| Bit | Description                              |
|-----|------------------------------------------|
| 31  | (reserved)                               |
| 23-18| HP_APM_M2_EXCEPTION_ID                  |
| 17  | HP_APM_M2_EXCEPTION_MODE                |
| 16  | HP_APM_M2_EXCEPTION_REGION              |
| 0   | Reset                                    |

HP_APM_M2_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M2_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
HP_APM_M2_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 16.17. HP_APM_M2_EXCEPTION_INFO1_REG (0x00F4)

| Bit | Description                              |
|-----|------------------------------------------|
| 31  | (reserved)                               |
| 0   | Reset                                    |

HP_APM_M2_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```