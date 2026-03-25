

```markdown
Register 18.68. CPU_APM_M1_EXCEPTION_INFO0_REG (0x00E0)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-24     | (reserved)                                 |                                                                             |
| 23        | CPU_APM_M1_EXCEPTION_REGION                | Represents the region where an exception occurs. (RO)                        |
| 18-16     | CPU_APM_M1_EXCEPTION_ID                    | Represents master ID when an exception occurs. (RO)                          |
| 17-16     | CPU_APM_M1_EXCEPTION_MODE                  | Represents the master's security mode when an exception occurs. (RO)         |
| 15        |                                             |                                                                             |

CPU_APM_M1_EXCEPTION_REGION  Represents the region where an exception occurs. (RO)
CPU_APM_M1_EXCEPTION_MODE    Represents the master's security mode when an exception occurs. (RO)
CPU_APM_M1_EXCEPTION_ID      Represents master ID when an exception occurs. (RO)

Register 18.69. CPU_APM_M1_EXCEPTION_INFO1_REG (0x00E4)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-0      | CPU_APM_M1_EXCEPTION_ADDR                 | Represents the access address when an exception occurs. (RO)                 |

CPU_APM_M1_EXCEPTION_ADDR  Represents the access address when an exception occurs. (RO)
```