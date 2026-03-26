

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| PMU_HP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in HP_SLEEP state                                              | 0x0098    | R/W    |
| PMU_HP_SLEEP_LP_REGULATORO_REG            | LP sys regulator control register in HP_SLEEP state                                            | 0x009C    | R/W    |
| PMU_HP_SLEEP_LP_DIG_POWER_REG             | LP system digital power domains control register in HP_SLEEP state                             | 0x00A8    | R/W    |
| PMU_HP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in HP_ACTIVE/HP_SLEEP state                            | 0x00AC    | R/W    |
| PMU_LP_SLEEP_LP_REGULATORO_REG            | LP sys regulator control register in HP_SLEEP state                                            | 0x00B4    | R/W    |
| PMU_LP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in LP_SLEEP state                                              | 0x00BC    | R/W    |
| PMU_LP_SLEEP_LP_DIG_POWER_REG             | Digital power domain control register in LP_SLEEP state                                       | 0x00C0    | R/W    |
| PMU_LP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in LP_SLEEP state                                      | 0x00C4    | R/W    |
| PMU_IMM_HP_CK_POWER_REG                   | Software control register for clock power                                                    | 0x00CC    | WT     |
| PMU_IMM_SLEEP_SYSCLK_REG                  | Software control register for system clock                                                   | 0x00D0    | WT     |
| PMU_IMM_HP_FUNC_ICG_REG                   | Software control register for peripheral clock                                                | 0x00D4    | WT     |
| PMU_IMM_HP_APB_ICG_REG                    | Software control register for APB clock                                                       | 0x00D8    | WT     |
| PMU_IMM_PAD_HOLD_ALL_REG                  | Software control register for PAD hold function                                               | 0x00E4    | varies |
| PMU_POWER_CK_WAIT_CNTL_REG                | Clock gating wait time configuration register                                                 | 0x011C    | R/W    |
| PMU_SLP_WAKEUP_CNTLO_REG                 | Sleep request register                                                                         | 0x0120    | WT     |
| PMU_SLP_WAKEUP_CNTL1_REG                  | Sleep reject register                                                                          | 0x0124    | R/W    |
| PMU_SLP_WAKEUP_CNTL2_REG                  | Wake up source enable register                                                                | 0x0128    | R/W    |
| PMU_SLP_WAKEUP_CNTL3_REG                  | Minimum sleep time control register                                                           | 0x012C    | R/W    |
| PMU_SLP_WAKEUP_CNTL4_REG                  | Sleep reject cause clear register                                                             | 0x0130    | WT     |
| PMU_SLP_WAKEUP_STATUSO_REG                | Wake up cause register                                                                         | 0x0144    | RO     |
| PMU_SLP_WAKEUP_STATUS1_REG                | Reset reject cause register                                                                    | 0x0148    | RO     |
| PMU_HP_CK_CNTL_REG                        | HP system clock control register                                                              | 0x0154    | R/W    |
| PMU_RF_PWC_REG                            | SAR ADC power up register                                                                      | 0x015C    | R/W    |
| PMU_INT_RAW_REG                           | PMU sleep/wake-up raw interrupt                                                                | 0x0164    | R/WTC/SS|
| PMU_HP_INT_ST_REG                         | PMU sleep/wake-up state interrupt                                                              | 0x0168    | RO     |
| PMU_HP_INT_ENA_REG                        | PMU sleep/wake-up interrupt enable register                                                    | 0x016C    | R/W    |
| PMU_HP_INT_CLR_REG                        | PMU sleep/wake-up interrupt clear register                                                     | 0x0170    | WT     |
| PMU_LP_INT_RAW_REG                        | PMU sleep/wake-up raw interrupt                                                                | 0x0174    | R/WTC/SS|
| PMU_LP_INT_ST_REG                         | PMU sleep/wake-up state interrupt                                                              | 0x0178    | RO     |
```