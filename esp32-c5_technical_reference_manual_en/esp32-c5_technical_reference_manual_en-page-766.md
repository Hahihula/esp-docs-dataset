

```markdown
Register 18.16. HP_APM_M2_EXCEPTION_INFO0_REG (0x00F0)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 23  | HP_APM_M2_EXCEPTION_ID                    | Represents master ID when an exception occurs. (RO)                         |
| 22  |                                            |                                                                             |
| 18  | HP_APM_M2_EXCEPTION_MODE                  | Represents the master's security mode when an exception occurs. (RO)         |
| 17  |                                            |                                                                             |
| 16  | HP_APM_M2_EXCEPTION_REGION                | Represents the region where an exception occurs. (RO)                       |
| 15  |                                            |                                                                             |
| 0   | Reset                                     |                                                                             |

HP_APM_M2_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M2_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
HP_APM_M2_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 18.17. HP_APM_M2_EXCEPTION_INFO1_REG (0x00F4)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | HP_APM_M2_EXCEPTION_ADDR                  | Represents the access address when an exception occurs. (RO)                 |
| 0   | Reset                                     |                                                                             |

HP_APM_M2_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```