

```markdown
Register 18.20. HP_APM_M3_EXCEPTION_INFO0_REG (0x0100)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 23-16| 0                                                                           |
| 15  | HP_APM_M3_EXCEPTION_MODE                                                   |
| 17  | HP_APM_M3_EXCEPTION_ID                                                     |
| 22  | HP_APM_M3_EXCEPTION_REGION                                                 |

HP_APM_M3_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M3_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
HP_APM_M3_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 18.21. HP_APM_M3_EXCEPTION_INFO1_REG (0x0104)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
|     | 0                                                                           |

HP_APM_M3_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```