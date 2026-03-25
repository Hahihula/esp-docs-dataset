

```markdown
Register 18.24. HP_APM_M4_EXCEPTION_INFO0_REG (0x0110)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 23-16 | HP_APM_M4_EXCEPTION_ID                  |
| 15-8 | HP_APM_M4_EXCEPTION_MODE                |
| 7-0  | HP_APM_M4_EXCEPTION_REGION              |

Reset: All bits are 0.

HP_APM_M4_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M4_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
HP_APM_M4_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 18.25. HP_APM_M4_EXCEPTION_INFO1_REG (0x0114)

| Bit | Field Name                                 |
|-----|--------------------------------------------|
| 31  | (reserved)                                |
| 31-8 | (reserved)                               |
| 7-0  | HP_APM_M4_EXCEPTION_ADDR                |

Reset: All bits are 0.

HP_APM_M4_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```