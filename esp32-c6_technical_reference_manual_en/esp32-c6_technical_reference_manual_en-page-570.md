

```markdown
| Name                                       | Description                                                                 | Address           | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-------------------|--------|
| LP_APM_REGIONn_ADDR_START_REG (n: 0-3)     | Region address register                                                    | 0x0004+0xC*n      | R/W    |
| LP_APM_REGIONn_ADDR_END_REG (n: 0-3)       | Region address register                                                    | 0x0008+0xC*n      | R/W    |

Region access authority attribute register
| LP_APM_REGIONn_ATTR_REG (n: 0-3)           | Region access authority attribute register                                 | 0x000C+0xC*n      | R/W    |
| function control register                  |                                                                             |                   |        |
| LP_APM_FUNC_CTRL_REG                       | APM function control register                                              | 0x00C4            | R/W    |

MO status register
| LP_APM_MO_STATUS_REG                      | MO status register                                                         | 0x00C8            | RO     |
| LP_APM_MO_STATUS_CLR_REG                  | MO status clear register                                                   | 0x00CC            | WT     |
| MO exception_info0 register               |                                                                             |                   |        |
| LP_APM_MO_EXCEPTION_INFO0_REG             | MO exception_info0 register                                                | 0x00D0            | RO     |
| MO exception_info1 register               |                                                                             |                   |        |
| LP_APM_MO_EXCEPTION_INFO1_REG             | MO exception_info1 register                                                | 0x00D4            | RO     |
| M1 status register                         |                                                                             |                   |        |
| LP_APM_M1_STATUS_REG                       | M1 status register                                                        | 0x00D8            | RO     |
| M1 status clear register                   |                                                                             |                   |        |
| LP_APM_M1_STATUS_CLR_REG                  | M1 status clear register                                                  | 0x00DC            | WT     |
| M1 exception_info0 register               |                                                                             |                   |        |
| LP_APM_M1_EXCEPTION_INFO0_REG             | M1 exception_info0 register                                               | 0x00E0            | RO     |
| M1 exception_info1 register               |                                                                             |                   |        |
| LP_APM_M1_EXCEPTION_INFO1_REG             | M1 exception_info1 register                                               | 0x00E4            | RO     |
| APM interrupt enable register              |                                                                             |                   |        |
| LP_APM_INT_EN_REG                          | APM interrupt enable register                                             | 0x00E8            | R/W    |
| clock gating register                      |                                                                             |                   |        |
| LP_APM_CLOCK_GATE_REG                     | clock gating register                                                     | 0x00EC            | R/W    |
| Version control register                  |                                                                             |                   |        |
| LP_APM_DATE_REG                           | Version control register                                                 | 0x00FC            | R/W    |

## 16.6.3 Low Power APMO Registers (LP_APMO_REG)

The addresses in this section are relative to the Access Permission Management Controller (HP_APM) base address + 0x1000 provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| Region filter enable register              |                                                                             |           |        |
| LP_APMO_REGION_FILTER_EN_REG             | Region filter enable register                                             | 0x0000    | R/W    |
| Region address register                    |                                                                             |           |        |
```