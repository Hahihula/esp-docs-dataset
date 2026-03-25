

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| PMU_HP_SLEEP_SYSCLK_REG                   | System clock control register in HP_SLEEP state                                                | 0x008C    | R/W    |
| PMU_HP_SLEEP_HP_REGULATORO_REG            | Regulator power control register in HP_SLEEP state                                             | 0x0090    | R/W    |
| PMU_HP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in HP_SLEEP state                                              | 0x0098    | R/W    |
| PMU_HP_SLEEP_LP_DIG_POWER_REG             | LP system digital power domains control register in HP_SLEEP state                             | 0x00A8    | R/W    |
| PMU_HP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in HP_ACTIVE/HP_SLEEP state                            | 0x00AC    | R/W    |
| PMU_LP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in LP_SLEEP state                                              | 0x00BC    | R/W    |
| PMU_LP_SLEEP_LP_DIG_POWER_REG             | Digital power domain control register in LP_SLEEP state                                        | 0x00C0    | R/W    |
| PMU_LP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in LP_SLEEP state                                       | 0x00C4    | R/W    |
| PMU_POWER_PD_MEM_MASK_REG                 | Internal SRAMx domain force power up                                                           | 0x0110    | R/W    |
| PMU_POWER_CK_WAIT_CNTL_REG                | Wait cycle for stable XTAL_CLK and PLL_CLK configuration register                              | 0x011C    | R/W    |
| PMU_SLP_WAKEUP_CNTL0_REG                  | Sleep request register                                                                         | 0x0120    | WT     |
| PMU_SLP_WAKEUP_CNTL1_REG                  | Sleep reject register                                                                          | 0x0124    | R/W    |
| PMU_SLP_WAKEUP_CNTL2_REG                  | Wake up source enable register                                                                 | 0x0128    | R/W    |
| PMU_SLP_WAKEUP_CNTL4_REG                  | Sleep reject cause clear register                                                              | 0x0130    | WT     |
| PMU_SLP_WAKEUP_STATUSO_REG                | Wake up cause register                                                                         | 0x0140    | RO     |
| PMU_SLP_WAKEUP_STATUS1_REG                | Reset reject cause register                                                                    | 0x0144    | RO     |
| PMU_RF_PWC_REG                            | SAR ADC power up register                                                                      | 0x0154    | R/W    |
| PMU_VDBAT_CFG_REG                         | VBAT mode configuration register                                                               | 0x0158    | varies |
| PMU_INT_RAW_REG                           | PMU sleep/wake-up raw interrupt                                                                | 0x0160    | R/WTC/SS|
| PMU_HP_INT_ST_REG                         | PMU sleep/wake-up state interrupt                                                              | 0x0164    | RO     |
| PMU_HP_INT_ENA_REG                        | PMU sleep/wake-up interrupt enable register                                                    | 0x0168    | R/W    |
| PMU_HP_INT_CLR_REG                        | PMU sleep/wake-up raw interrupt clear register                                                 | 0x016C    | WT     |
| PMU_DATE_REG                              | Version control register                                                                       | 0x03FC    | R/W    |

## 11.9.2 Always-on Register Summary

The addresses in this section are relative to the Always-on Registers base address provided in Table 4.3-2 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```