

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| PMU_POWER_CK_WAIT_CNTL_REG                 | Configuration register for system waiting time after clock change controlled by PMU              | 0x0120    | R/W    |
| PMU_SLP_WAKEUP_CNTL0_REG                   | Sleep request register                                                                           | 0x0124    | WT     |
| PMU_SLP_WAKEUP_CNTL1_REG                   | Sleep reject register                                                                            | 0x0128    | R/W    |
| PMU_SLP_WAKEUP_CNTL2_REG                   | Wakeup source enable register                                                                    | 0x012C    | R/W    |
| PMU_SLP_WAKEUP_CNTL3_REG                   | PMU state selection signal and waiting time register for sleep-Wakeup                          | 0x0130    | R/W    |
| PMU_SLP_WAKEUP_CNTL4_REG                   | Sleep reject event clear register                                                               | 0x0134    | WT     |
| PMU_SLP_WAKEUP_CNTL5_REG                   | Waiting time register after Wakeup in LP_SLEEP and HP_SLEEP                                   | 0x0138    | R/W    |
| PMU_SLP_WAKEUP_CNTL6_REG                   | Waiting time register after Wakeup in HP_MODEM phase                                          | 0x013C    | R/W    |
| PMU_SLP_WAKEUP_CNTL7_REG                   | Waiting time register after Wakeup in HP_SWITCH phase                                         | 0x0140    | R/W    |
| PMU_SLP_WAKEUP_STATUS0_REG                 | Wakeup event register                                                                            | 0x0144    | RO     |
| PMU_SLP_WAKEUP_STATUS1_REG                 | Reset reject event register                                                                     | 0x0148    | RO     |
| PMU_HP_CK_CNTL_REG                         | PMU-set waiting time after ICG configuration adjustment                                       | 0x0150    | R/W    |
| PMU_RF_PWC_REG                             | Configuration for i2c and rf circuits controlled by PMU                                        | 0x0158    | R/W    |
| PMU_BACKUP_CFG_REG                         | Configuration for backup clock frequency division controlled by PMU                           | 0x015C    | R/W    |
| PMU_INT_RAW_REG                             | PMU sleep/Wakeup raw interrupt                                                                  | 0x0160    | R/WTC/SS|
| PMU_HP_INT_ST_REG                           | PMU sleep/Wakeup status interrupt                                                               | 0x0164    | RO     |
| PMU_HP_INT_ENA_REG                          | PMU sleep/Wakeup interrupt enable                                                              | 0x0168    | R/W    |
| PMU_HP_INT_CLR_REG                          | PMU sleep/Wakeup interrupt clear                                                                | 0x016C    | WT     |
| PMU_LP_INT_RAW_REG                          | Low-power system raw interrupt                                                                  | 0x0170    | R/WTC/SS|
| PMU_LP_INT_ST_REG                           | PMU state transition interrupt status                                                          | 0x0174    | RO     |
| PMU_LP_INT_ENA_REG                          | PMU state transition interrupt enable                                                          | 0x0178    | R/W    |
| PMU_LP_INT_CLR_REG                          | PMU state transition interrupt clear                                                           | 0x017C    | WT     |
| PMU_HP_REGULATOR_CFG_REG                    | PMU-controlled update of digital regulator configuration                                      | 0x018C    | R/W    |
| PMU_DATE_REG                                | Version control                                                                                  | 0x01A8    | R/W    |

### 11.8.2 PAU Register Summary

The addresses in this section below are relative to the PAU base address provided in Table 4.3-2 in Chapter 4 System and Memory.

| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| Control & Configuration Register           |                                                            |           |        |
| PAU_REGDMA_CONF_REG                        | Peripherals backup configuration/control register                                               | 0x0000    | varies |
```