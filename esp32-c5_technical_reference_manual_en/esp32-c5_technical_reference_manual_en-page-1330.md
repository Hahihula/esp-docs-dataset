

```markdown
| Name                                 | Description                                                                                   | Address   | Access |
|--------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| **Configuration Register**           |                                                                                               |           |        |
| PCNT_U0_CONF0_REG                    | Configuration register 0 for unit 0                                                          | 0x0000    | R/W    |
| PCNT_U0_CONF1_REG                    | Configuration register 1 for unit 0                                                          | 0x0004    | R/W    |
| PCNT_U0_CONF2_REG                    | Configuration register 2 for unit 0                                                          | 0x0008    | R/W    |
| PCNT_U0_CONF3_REG                    | Configuration register for unit 0’s step value.                                             | 0x000C    | R/W    |
| PCNT_U1_CONF0_REG                    | Configuration register 0 for unit 1                                                          | 0x0010    | R/W    |
| PCNT_U1_CONF1_REG                    | Configuration register 1 for unit 1                                                          | 0x0014    | R/W    |
| PCNT_U1_CONF2_REG                    | Configuration register 2 for unit 1                                                          | 0x0018    | R/W    |
| PCNT_U1_CONF3_REG                    | Configuration register for unit 1’s step value.                                             | 0x001C    | R/W    |
| PCNT_U2_CONF0_REG                    | Configuration register 0 for unit 2                                                          | 0x0020    | R/W    |
| PCNT_U2_CONF1_REG                    | Configuration register 1 for unit 2                                                          | 0x0024    | R/W    |
| PCNT_U2_CONF2_REG                    | Configuration register 2 for unit 2                                                          | 0x0028    | R/W    |
| PCNT_U2_CONF3_REG                    | Configuration register for unit 2’s step value.                                             | 0x002C    | R/W    |
| PCNT_U3_CONF0_REG                    | Configuration register 0 for unit 3                                                          | 0x0030    | R/W    |
| PCNT_U3_CONF1_REG                    | Configuration register 1 for unit 3                                                          | 0x0034    | R/W    |
| PCNT_U3_CONF2_REG                    | Configuration register 2 for unit 3                                                          | 0x0038    | R/W    |
| PCNT_U3_CONF3_REG                    | Configuration register for unit 3’s step value.                                             | 0x003C    | R/W    |
| PCNT_CTRL_REG                        | Control register for all counters                                                            | 0x0070    | R/W    |
| **Status Register**                  |                                                                                               |           |        |
| PCNT_U0_CNT_REG                      | Counter value for unit 0                                                                      | 0x0040    | RO     |
| PCNT_U1_CNT_REG                      | Counter value for unit 1                                                                      | 0x0044    | RO     |
| PCNT_U2_CNT_REG                      | Counter value for unit 2                                                                      | 0x0048    | RO     |
| PCNT_U3_CNT_REG                      | Counter value for unit 3                                                                      | 0x004C    | RO     |
| PCNT_U0_STATUS_REG                   | PNCT UNIT0 status register                                                                   | 0x0060    | RO     |
| PCNT_U1_STATUS_REG                   | PNCT UNIT1 status register                                                                   | 0x0064    | RO     |
| PCNT_U2_STATUS_REG                   | PNCT UNIT2 status register                                                                   | 0x0068    | RO     |
| PCNT_U3_STATUS_REG                   | PNCT UNIT3 status register                                                                   | 0x006C    | RO     |
| **Interrupt Register**               |                                                                                               |           |        |
| PCNT_INT_RAW_REG                     | Interrupt raw status register                                                                | 0x0050    | R/WTC/SS|
| PCNT_INT_ST_REG                       | Interrupt status register                                                                    | 0x0054    | RO     |
| PCNT_INT_ENA_REG                     | Interrupt enable register                                                                    | 0x0058    | R/W    |
| PCNT_INT_CLR_REG                     | Interrupt clear register                                                                     | 0x005C    | WT     |
| **Version Register**                 |                                                                                               |           |        |
| PCNT_DATE_REG                        | PNCT version control register                                                                | 0x00FC    | R/W    |
```