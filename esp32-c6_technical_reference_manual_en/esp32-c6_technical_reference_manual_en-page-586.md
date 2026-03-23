

```markdown
Register 16.36. LP_APM_M1_EXCEPTION_INFO0_REG (0x00E0)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | (reserved)                                |
| 23..18    | LP_APM_M1_EXCEPTION_ID                    |
| 17..16    | LP_APM_M1_EXCEPTION_MODE                  |
| 15..4     | (reserved)                               |
| 3         | Reset                                     |

LP_APM_M1_EXCEPTION_REGION Represents exception region. (RO)
LP_APM_M1_EXCEPTION_MODE Represents exception mode. (RO)
LP_APM_M1_EXCEPTION_ID Represents exception id information. (RO)

Register 16.37. LP_APM_M1_EXCEPTION_INFO1_REG (0x00E4)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | LP_APM_M1_EXCEPTION_ADDR                  |
|           | Reset                                     |

LP_APM_M1_EXCEPTION_ADDR Represents exception addr. (RO)
```