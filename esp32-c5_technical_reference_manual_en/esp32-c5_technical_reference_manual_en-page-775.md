

```markdown
## Register 18.36. LP_APM_MO_EXCEPTION_INFO0_REG (0x00D0)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31-24     | (reserved)                                |
| 23        | LP_APM_MO_EXCEPTION_REGION                |
| 22        |                                            |
| 18-16     | LP_APM_MO_EXCEPTION_ID                    |
| 15-0      | LP_APM_MO_EXCEPTION_MODE                  |

LP_APM_MO_EXCEPTION_REGION Represents the region where an exception occurs. (RO)

LP_APM_MO_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)

LP_APM_MO_EXCEPTION_ID Represents master ID when an exception occurs. (RO)


## Register 18.37. LP_APM_MO_EXCEPTION_INFO1_REG (0x00D4)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | LP_APM_MO_EXCEPTION_ADDR                  |
| 0         |                                            |

LP_APM_MO_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)


## Register 18.38. LP_APM_M1_STATUS_REG (0x00D8)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | (reserved)                                |
| 2         | LP_APM_M1_EXCEPTION_STATUS                |
| 1         |                                            |
| 0         | Reset                                     |

LP_APM_M1_EXCEPTION_STATUS Represents exception status.
bit0: 1 represents permission restrictions
bit1: 1 represents address out of bounds
(RO)
```