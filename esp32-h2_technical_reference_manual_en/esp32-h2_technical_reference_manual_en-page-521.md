

```markdown
Register 15.16. HP_APM_M2_EXCEPTION_INFO0_REG (0x00F0)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | (reserved)                                |
| 23..22    |                                            |
| 18..17    | HP_APM_M2_EXCEPTION_ID                    |
| 16..15    | HP_APM_M2_EXCEPTION_MODE                  |
| 0         | HP_APM_M2_EXCEPTION_REGION                |

Reset: All bits are 0.

HP_APM_M2_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
HP_APM_M2_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
HP_APM_M2_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 15.17. HP_APM_M2_EXCEPTION_INFO1_REG (0x00F4)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31..0     | HP_APM_M2_EXCEPTION_ADDR                  |

Reset: All bits are 0.

HP_APM_M2_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)
```