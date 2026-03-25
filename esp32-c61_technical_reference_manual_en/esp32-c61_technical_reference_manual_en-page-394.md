

```markdown
| No. | Chapter                  | Interrupt Source                          | Interrupt Source Mapping Register                     | Bit | Interrupt Status Register Name |
|-----|--------------------------|-------------------------------------------|--------------------------------------------------------|-----|--------------------------------|
| 0   | n/a                      | reserved                                  | reserved                                                | 0   |                                |
| 1   | n/a                      | reserved                                  | reserved                                                | 1   |                                |
| 2   | n/a                      | reserved                                  | reserved                                                | 2   |                                |
| 3   | n/a                      | reserved                                  | reserved                                                | 3   |                                |
| 4   | n/a                      | reserved                                  | reserved                                                | 4   |                                |
| 5   | n/a                      | reserved                                  | reserved                                                | 5   |                                |
| 6   | n/a                      | reserved                                  | reserved                                                | 6   |                                |
| 7   | n/a                      | reserved                                  | reserved                                                | 7   |                                |
| 8   | n/a                      | reserved                                  | reserved                                                | 9   |                                |
| 9   | n/a                      | reserved                                  | reserved                                                | 9   |                                |
| 10  | n/a                      | reserved                                  | reserved                                                | 10  |                                |
| 11  | n/a                      | reserved                                  | reserved                                                | 11  |                                |
| 12  | n/a                      | reserved                                  |                                                        |     |                                |
| 13  | Low-Power Management     | PMU_INTR                                  | INTMTX_COREO_PPMU_INTR_MAP_REG                         | 13  |                                |
| 14  | eFuse Controller (EFUSE) | EFUSE_INTR                                | INTMTX_COREO_EFUSE_INTR_MAP_REG                        | 14  |                                |
| 15  | Low-Power Management     | LP_RTC_TIMER_INTR                         | INTMTX_COREO_LP_RTC_TIMER_INTR_MAP_REG                 | 15  | INTMTX_COREO_INT_STATUS_0_REG |
| 16  | Low-Power Management     | LP_WDT_INTR                               | INTMTX_COREO_LP_WDT_INTR_MAP_REG                       | 16  |                                |
| 17  | System Registers         | LP_PERI_TIMEOUT_INTR                      | INTMTX_COREO_LP_PERI_TIMEOUT_INTR_MAP_REG              | 17  |                                |
| 18  | Permission Control (PMS) | LLP_APM_MO_INTR                           | INTMTX_COREO_LLP_APM_MO_INTR_MAP_REG                   | 18  |                                |
| 19  | Software Interrupt Registers | CPU_INTR_FROM_CPU_0                    | INTMTX_COREO_CPU_INTR_FROM_CPU_0_MAP_REG               | 19  |                                |
| 20  | Software Interrupt Registers | CPU_INTR_FROM_CPU_1                    | INTMTX_COREO_CPU_INTR_FROM_CPU_1_MAP_REG               | 20  |                                |
| 21  | Software Interrupt Registers | CPU_INTR_FROM_CPU_2                    | INTMTX_COREO_CPU_INTR_FROM_CPU_2_MAP_REG               | 21  |                                |
| 22  | ESP-RISC-V CPU           | CPU_INTR_FROM_CPU_3                    | INTMTX_COREO_CPU_INTR_FROM_CPU_3_MAP_REG               | 22  |                                |
| 23  | Debug Assistant          | ASSIST_DEBUG_INTR                         | INTMTX_COREO_ASSIST_DEBUG_INTR_MAP_REG                 | 23  |                                |
| 24  | ESP-RISC-V CPU           | TRACE_INTR                               | INTMTX_COREO_TRACE_INTR_MAP_REG                        | 24  |                                |
| 25  | n/a                      | reserved                                  |                                                        |     |                                |
| 26  | System Registers         | CPU_PERI_TIMEOUT_INTR                     | INTMTX_COREO_CPU_PERI_TIMEOUT_INTR_MAP_REG             | 26  |                                |
| 27  | GPIO Matrix and IO MUX   | GPIO_INTR_PRO                             | INTMTX_COREO_GPIO_INTR_PRO_MAP_REG                     | 27  |                                |
| 28  | GPIO Matrix and IO MUX   | GPIO_INTR_EXT                             | INTMTX_COREO_GPIO_INTR_EXT_MAP_REG                     | 28  |                                |
| 29  | Low-Power Management     | PAU_INTR                                  | INTMTX_COREO_PAU_INTR_MAP_REG                          | 29  |                                |
| 30  | System Registers         | HP_PERI_TIMEOUT_INTR                      | INTMTX_COREO_HP_PERI_TIMEOUT_INTR_MAP_REG              | 30  |                                |
| 31  | n/a                      | reserved                                  |                                                        |     |                                |
| 32  | Permission Control (PMS) | HP_APM_MO_INTR                            | INTMTX_COREO_HP_APM_MO_INTR_MAP_REG                    | 0   | INTMTX_COREO_INT_STATUS_1_REG |
| 33  | Permission Control (PMS) | HP_APM_M1_INTR                            | INTMTX_COREO_HP_APM_M1_INTR_MAP_REG                    | 1   |                                |
| 34  | Permission Control (PMS) | HP_APM_M2_INTR                            | INTMTX_COREO_HP_APM_M2_INTR_MAP_REG                    | 2   |                                |
| 35  | Permission Control (PMS) | HP_APM_M3_INTR                            | INTMTX_COREO_HP_APM_M3_INTR_MAP_REG                    | 3   |                                |
| 36  | Permission Control (PMS) | CPU_APM_MO_INTR                           | INTMTX_COREO_CPU_APM_MO_INTR_MAP_REG                   | 4   |                                |
```