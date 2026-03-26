

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| PMU_LP_INT_ENA_REG                         | PMU sleep/wake-up interrupt enable register                                | 0x017C  | R/W    |
| PMU_LP_INT_CLR_REG                         | PMU sleep/wake-up interrupt clear register                                 | 0x0180  | varies |
| PMU_LP_CPU_PWR0_REG                        | LP CPU sleep/wake-up control register                                     | 0x0184  | varies |
| PMU_LP_CPU_PWR1_REG                        | LP CPU sleep/wake-up control register                                     | 0x0188  | WT     |
| PMU_LP_CPU_PWR2_REG                        | LP CPU sleep/wake-up control register                                     | 0x018C  | R/W    |
| PMU_LP_CPU_PWR3_REG                        | LP CPU sleep/wake-up control register                                     | 0x0190  | RO     |
| PMU_LP_CPU_PWR4_REG                        | LP CPU sleep/wake-up control register                                     | 0x0194  | R/W    |
| PMU_LP_CPU_PWR5_REG                        | LP CPU sleep/wake-up control register                                     | 0x0198  | RO     |
| PMU_HP_LP_CPU_COMM_REG                     | LP CPU sleep/wake-up control register                                     | 0x019C  | WT     |
| PMU_EXT_LDO_PO_OP1A_REG                    | VO1 regulator control register                                            | 0x01B8  | R/W    |
| PMU_EXT_LDO_PO_OP1A_ANA_REG                | VO1 regulator control register                                            | 0x01BC  | R/W    |
| PMU_EXT_LDO_PO_OP2A_REG                    | VO3 regulator control register                                            | 0x01CO  | R/W    |
| PMU_EXT_LDO_PO_OP2A_ANA_REG                | VO3 regulator control register                                            | 0x01C4  | R/W    |
| PMU_EXT_LDO_P1_OP1A_REG                    | VO2 regulator control register                                            | 0x01DO  | R/W    |
| PMU_EXT_LDO_P1_OP1A_ANA_REG                | VO2 regulator control register                                            | 0x01D4  | R/W    |
| PMU_EXT_LDO_P1_OP2A_REG                    | VO4 regulator control register                                            | 0x01D8  | R/W    |
| PMU_EXT_LDO_P1_OP2A_ANA_REG                | VO4 regulator control register                                            | 0x01DC  | R/W    |
| PMU_EXT_WAKEUP_LV_REG                      | EXT wake-up level control register                                        | 0x01E8  | R/W    |
| PMU_EXT_WAKEUP_SEL_REG                     | EXT wake-up IO control register                                           | 0x01EC  | R/W    |
| PMU_EXT_WAKEUP_ST_REG                      | EXT wake-up status register                                               | 0x01FO  | RO     |
| PMU_EXT_WAKEUP_CNTL_REG                    | EXT wake-up control register                                              | 0x01F4  | R/W    |
| PMU_SDIO_WAKEUP_CNTL_REG                   | SDIO wake-up control register                                             | 0x01F8  | R/W    |
| PMU_TOUCH_PWR_CNTL_REG                     | TOUCH sleep/wake-up control register                                      | 0x0210  | R/W    |
| PMU_DATE_REG                               | Version control register                                                  | 0x03FC  | R/W    |
```