

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| PMU_POWER_CK_WAIT_CNTL_REG                 | Wait cycle for stable XTAL_CLK and PLL_CLK configuration register                               | 0x0120  | R/W    |
| PMU_SLP_WAKEUP_CNTLO_REG                   | Sleep request register                                                                          | 0x0124  | WT     |
| PMU_SLP_WAKEUP_CNTL1_REG                   | Sleep reject register                                                                           | 0x0128  | R/W    |
| PMU_SLP_WAKEUP_CNTL2_REG                   | Wake up source enable register                                                                  | 0x012C  | R/W    |
| PMU_SLP_WAKEUP_CNTL4_REG                   | Sleep reject cause clear register                                                               | 0x0134  | WT     |
| PMU_SLP_WAKEUP_STATUSO_REG                 | Wake up cause register                                                                          | 0x0144  | RO     |
| PMU_SLP_WAKEUP_STATUS1_REG                 | Reset reject cause register                                                                     | 0x0148  | RO     |
| PMU_INT_RAW_REG                            | PMU sleep/wake-up raw interrupt                                                                 | 0x0160  | R/WTC/SS|
| PMU_HP_INT_ST_REG                          | PMU sleep/wake-up state interrupt                                                               | 0x0164  | RO     |
| PMU_HP_INT_ENA_REG                         | PMU sleep/wake-up interrupt enable register                                                    | 0x0168  | R/W    |
| PMU_HP_INT_CLR_REG                         | PMU sleep/wake-up raw interrupt clear register                                                  | 0x016C  | WT     |
| PMU_LP_INT_RAW_REG                         | Low-power system raw interrupt                                                                  | 0x0170  | R/WTC/SS|
| PMU_LP_INT_ST_REG                          | PMU state switch interrupt state register                                                      | 0x0174  | RO     |
| PMU_LP_INT_ENA_REG                         | PMU state switch interrupt enable register                                                     | 0x0178  | R/W    |
| PMU_LP_INT_CLR_REG                         | PMU state switch interrupt clear register                                                      | 0x017C  | WT     |
| PMU_LP_CPU_PWR0_REG                        | LP CPU control register                                                                         | 0x0180  | R/W    |
| PMU_LP_CPU_PWR1_REG                        | LP CPU sleep request register                                                                   | 0x0184  | varies |
| PMU_HP_LP_CPU_COMM_REG                     | Software interrupt register                                                                     | 0x0188  | WT     |
| PMU_DATE_REG                               | Version control register                                                                        | 0x01A8  | R/W    |

### 13.9.2 Always-on Register Summary

The addresses in this section are relative to the Always-on Registers base address provided in Table 6.3-2 in Chapter 6 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| Configuration Registers                    |                                                                                                  |         |        |
| LP_AON_STORE0_REG                          | Always-on register0                                                                              | 0x0000  | R/W    |
| LP_AON_STORE1_REG                          | Always-on register1                                                                              | 0x0004  | R/W    |
| LP_AON_STORE2_REG                          | Always-on register2                                                                              | 0x0008  | R/W    |
| LP_AON_STORE3_REG                          | Always-on register3                                                                              | 0x000C  | R/W    |
| LP_AON_STORE4_REG                          | Always-on register4                                                                              | 0x0010  | R/W    |
| LP_AON_STORE5_REG                          | Always-on register5                                                                              | 0x0014  | R/W    |
| LP_AON_STORE6_REG                          | Always-on register6                                                                              | 0x0018  | R/W    |
| LP_AON_STORE7_REG                          | Always-on register7                                                                              | 0x001C  | R/W    |
| LP_AON_STORE8_REG                          | Always-on register8                                                                              | 0x0020  | R/W    |
```