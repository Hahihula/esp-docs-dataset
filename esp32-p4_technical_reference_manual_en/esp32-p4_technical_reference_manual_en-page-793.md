
```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| COREO_DMA2D_OUT_CH3_INT_MAP_REG           | DMA2D_OUT_CH3_INTR mapping register                                                             | 0x218   | R/W    |
| COREO_AXI_PERF_MON_INT_MAP_REG            | AXI_PERF_MON_INTR mapping register                                                              | 0x21C   | R/W    |
| COREO_INTR_STATUS_REG_4_REG               | Status register for interrupt sources 128 ~ 130                                                | 0x0220  | RO     |
| COREO_INTR_SIG_IDX_ASSERT_IN_SEC_REG      | Interrupt delegation configuration register for COREO                                           | 0x0228  | R/W    |
| COREO_INTR_SEC_STATUS_REG                 | Interrupt delegation status register for COREO                                                  | 0x022C  | RO     |
| COREO_INTR_SRC_PAS_IN_SEC_STATUS_O_REG    | Interrupt delegation status register for interrupt sources 0 ~ 31                                | 0x0230  | RO     |
| COREO_INTR_SRC_PAS_IN_SEC_STATUS_1_REG     | Interrupt delegation status register for interrupt sources 32 ~ 63                              | 0x0234  | RO     |
| COREO_INTR_SRC_PAS_IN_SEC_STATUS_2_REG     | Interrupt delegation status register for interrupt sources 64 ~ 95                              | 0x0238  | RO     |
| COREO_INTR_SRC_PAS_IN_SEC_STATUS_3_REG     | Interrupt delegation status register for interrupt sources 96 ~ 127                             | 0x023C  | RO     |
| COREO_INTR_SRC_PAS_IN_SEC_STATUS_4_REG     | Interrupt delegation status register for interrupt sources 128 ~ 130                            | 0x0240  | RO     |
| COREO_INTERRUPT_REG_DATE_REG              | Version control register                                                                        | 0x03FC  | R/W    |

### 12.5.2 HP CPU1 Interrupt Matrix Register Summary

| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| CORE1_LP_RTC_INT_MAP_REG                  | LP_RTC_INTR mapping register                                                                     | 0x0000  | R/W    |
| CORE1_LP_WDT_INT_MAP_REG                  | LP_WDT_INTR mapping register                                                                     | 0x0004  | R/W    |
| CORE1_LP_TIMER_REG_O_INT_MAP_REG          | LP_TIMER_REG_O_INTR mapping register                                                            | 0x0008  | R/W    |
| CORE1_LP_TIMER_REG_1_INT_MAP_REG          | LP_TIMER_REG_1_INTR mapping register                                                           | 0x000C  | R/W    |
| CORE1_MB_HP_INT_MAP_REG                   | MB_HP_INTR mapping register                                                                      | 0x0010  | R/W    |
| CORE1_MB_LP_INT_MAP_REG                   | MB_LP_INTR mapping register                                                                      | 0x0014  | R/W    |
| CORE1_PMU_REG_O_INT_MAP_REG               | PMU_REG_O_INTR mapping register                                                                  | 0x0018  | R/W    |
```