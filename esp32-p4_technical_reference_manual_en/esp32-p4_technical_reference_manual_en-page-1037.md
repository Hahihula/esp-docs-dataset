

```markdown
Register 14.45. PMU_HP_INT_ENA_REG (0x016C)

| Bit | Field Name                                                                 | Description                                                                 |
|-----|---------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| 31  | PMU_SOC_WAKEUP_INT_ENA                                                   | Write 1 to enable PMU_SOC_WAKEUP_INT. (R/W)                                 |
| 30  | PMU_SOC_SLEEP_REJECT_INT_ENA                                             | Write 1 to enable PMU_SOC_SLEEP_REJECT_INT. (R/W)                           |
| 29  | PMU_SW_INT_ENA                                                            | Write 1 to enable PMU_SW_INT. (R/W)                                         |
| 28  | PMU_SDIO_IDLE_INT_ENA                                                    | Write 1 to enable PMU_SDIO_IDLE_INT. (R/W)                                  |
| 27  | PMU_LP_CPU_EXC_INT_ENA                                                   | Write 1 to enable PMU_LP_CPU_EXC_INT. (R/W)                                 |
| 26  | (reserved)                                                               |                                                                             |
| 25  | (reserved)                                                               |                                                                             |
| 24  | (reserved)                                                               |                                                                             |
| 23  | (reserved)                                                               |                                                                             |
| 22  | PMU_OP1A_CNT_TARGET0_REACH_O_HP_INT_ENA Write 1 to enable                 | PMU_OP1A_CNT_TARGET0_REACH_O_INT. (R/W)                                     |
| 21  | PMU_OP1A_CNT_TARGET1_REACH_O_HP_INT_ENA Write 1 to enable                 | PMU_OP1A_CNT_TARGET1_REACH_O_INT. (R/W)                                     |
| 20  | PMU_OP1A_CNT_TARGET0_REACH_1_HP_INT_ENA Write 1 to enable                 | PMU_OP1A_CNT_TARGET0_REACH_1_INT. (R/W)                                     |
| 19  | PMU_OP1A_CNT_TARGET1_REACH_1_HP_INT_ENA Write 1 to enable                 | PMU_OP1A_CNT_TARGET1_REACH_1_INT. (R/W)                                     |
| 18  | PMU_OP2A_CNT_TARGET0_REACH_O_HP_INT_ENA Write 1 to enable                 | PMU_OP2A_CNT_TARGET0_REACH_O_INT. (R/W)                                     |
| 17  | PMU_OP2A_CNT_TARGET1_REACH_O_HP_INT_ENA Write 1 to enable                 | PMU_OP2A_CNT_TARGET1_REACH_O_INT. (R/W)                                     |
| 16  | PMU_OP2A_CNT_TARGET0_REACH_1_HP_INT_ENA Write 1 to enable                 | PMU_OP2A_CNT_TARGET0_REACH_1_INT. (R/W)                                     |
| 15  | PMU_OP2A_CNT_TARGET1_REACH_1_HP_INT_ENA Write 1 to enable                 | PMU_OP2A_CNT_TARGET1_REACH_1_INT. (R/W)                                     |
| 14  | (reserved)                                                               |                                                                             |
| 13  | (reserved)                                                               |                                                                             |
| 12  | (reserved)                                                               |                                                                             |
| 11  | (reserved)                                                               |                                                                             |
| 10  | (reserved)                                                               |                                                                             |
| 9   | (reserved)                                                               |                                                                             |
| 8   | (reserved)                                                               |                                                                             |
| 7   | (reserved)                                                               |                                                                             |
| 6   | (reserved)                                                               |                                                                             |
| 5   | (reserved)                                                               |                                                                             |
| 4   | (reserved)                                                               |                                                                             |
| 3   | (reserved)                                                               |                                                                             |
| 2   | (reserved)                                                               |                                                                             |
| 1   | (reserved)                                                               |                                                                             |
| 0   | Reset                                                                    | 0                                                                               |

PMU_OP1A_CNT_TARGET0_REACH_O_HP_INT_ENA Write 1 to enable PMU_OP1A_CNT_TARGET0_REACH_O_INT. (R/W)
PMU_OP1A_CNT_TARGET1_REACH_O_HP_INT_ENA Write 1 to enable PMU_OP1A_CNT_TARGET1_REACH_O_INT. (R/W)
PMU_OP1A_CNT_TARGET0_REACH_1_HP_INT_ENA Write 1 to enable PMU_OP1A_CNT_TARGET0_REACH_1_INT. (R/W)
PMU_OP1A_CNT_TARGET1_REACH_1_HP_INT_ENA Write 1 to enable PMU_OP1A_CNT_TARGET1_REACH_1_INT. (R/W)

PMU_OP2A_CNT_TARGET0_REACH_O_HP_INT_ENA Write 1 to enable PMU_OP2A_CNT_TARGET0_REACH_O_INT. (R/W)
PMU_OP2A_CNT_TARGET1_REACH_O_HP_INT_ENA Write 1 to enable PMU_OP2A_CNT_TARGET1_REACH_O_INT. (R/W)
PMU_OP2A_CNT_TARGET0_REACH_1_HP_INT_ENA Write 1 to enable PMU_OP2A_CNT_TARGET0_REACH_1_INT. (R/W)
PMU_OP2A_CNT_TARGET1_REACH_1_HP_INT_ENA Write 1 to enable PMU_OP2A_CNT_TARGET1_REACH_1_INT. (R/W)

PMU_LP_CPU_EXC_INT_ENA Write 1 to enable PMU_LP_CPU_EXC_INT. (R/W)
PMU_SDIO_IDLE_INT_ENA Write 1 to enable PMU_SDIO_IDLE_INT. (R/W)
PMU_SW_INT_ENA Write 1 to enable PMU_SW_INT. (R/W)
PMU_SOC_SLEEP_REJECT_INT_ENA Write 1 to enable PMU_SOC_SLEEP_REJECT_INT. (R/W)
PMU_SOC_WAKEUP_INT_ENA Write 1 to enable PMU_SOC_WAKEUP_INT. (R/W)
```