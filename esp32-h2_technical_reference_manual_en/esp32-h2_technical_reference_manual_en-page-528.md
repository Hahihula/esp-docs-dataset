

```markdown
Register 15.32. LP_APM_MO_EXCEPTION_INFOO_REG (0x00D0)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | (reserved)                                |
| 23..18    | LP_APM_MO_EXCEPTION_ID                    |
| 17..16    | LP_APM_MO_EXCEPTION_MODE                  |
| 4..0      | LP_APM_MO_EXCEPTION_REGION                |

LP_APM_MO_EXCEPTION_REGION Represents the region where an exception occurs. (RO)
LP_APM_MO_EXCEPTION_MODE Represents the master's security mode when an exception occurs. (RO)
LP_APM_MO_EXCEPTION_ID Represents master ID when an exception occurs. (RO)

Register 15.33. LP_APM_MO_EXCEPTION_INFO1_REG (0x00D4)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31..0     | LP_APM_MO_EXCEPTION_ADDR                  |

LP_APM_MO_EXCEPTION_ADDR Represents the access address when an exception occurs. (RO)

Register 15.34. LP_APM_INT_EN_REG (0x00E8)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 30        | LP_APM_MO_APM_INT_EN                      |

LP_APM_MO_APM_INT_EN Configures to enable LP_APM_CTRL MO interrupt.
0: Disable
1: Enable
(R/W)
```