

```markdown
Register 16.48. CPU_APM_M1_EXCEPTION_INFO0_REG (0x00E0)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31-24     | (reserved)                                |
| 23        | O                                         |
| 18-16     | CPU_APM_M1_EXCEPTION_ID                   |
| 15        | CPU_APM_M1_EXCEPTION_MODE                 |
| 0         | CPU_APM_M1_EXCEPTION_REGION               |

CPU_APM_M1_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
CPU_APM_M1_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
CPU_APM_M1_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 16.49. CPU_APM_M1_EXCEPTION_INFO1_REG (0x00E4)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31-0      | CPU_APM_M1_EXCEPTION_ADDR                 |

CPU_APM_M1_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```