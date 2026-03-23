

```markdown
Register 16.48. LP_APMO_MO_EXCEPTION_INFO0_REG (0x00D0)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | (reserved)                                |
| 23..17    | (reserved)                                |
| 16..15    | LP_APMO_MO_EXCEPTION_ID                   |
| 14..8     | LP_APMO_MO_EXCEPTION_MODE                 |
| 7         | (reserved)                                |
| 6         | (reserved)                                |
| 5         | (reserved)                                |
| 4         | (reserved)                                |
| 3         | (reserved)                                |
| 2         | (reserved)                                |
| 1         | (reserved)                                |
| 0         | LP_APMO_MO_EXCEPTION_REGION               |

LP_APMO_MO_EXCEPTION_REGION Represents exception region (RO)
LP_APMO_MO_EXCEPTION_MODE Represents exception mode (RO)
LP_APMO_MO_EXCEPTION_ID Represents exception id information (RO)

Register 16.49. LP_APMO_MO_EXCEPTION_INFO1_REG (0x00D4)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31        | (reserved)                                |
| 0         | LP_APMO_MO_EXCEPTION_ADDR                 |

LP_APMO_MO_EXCEPTION_ADDR Represents exception addr (RO)

Register 16.50. LP_APMO_MO_INT_EN_REG (0x00D8)

| Bit Range | Field Name                                 |
|-----------|--------------------------------------------|
| 31..29    | (reserved)                                |
| 28        | LP_APMO_MO_APM_INT_EN                     |
| 27..0     | Reset                                      |

LP_APMO_MO_APM_INT_EN Configures APM MO interrupt enable.
0: disable
1: enable
(R/W)
```