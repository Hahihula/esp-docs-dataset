

```markdown
Register 14.46. PMU_HP_INT_CLR_REG (0x0170)

| Bit | Field Description                                                                 |
|-----|------------------------------------------------------------------------------------|
| 31  | 30   | 29   | 28   | 27   | 26   | 25   | 24   | 23   | 22   | 21   | 20   | 19   | 18   | 17   | 16   | 15   | 14   | 13   | 12   | ... | 0    |
|-----|------|------|------|------|------|------|------|------|------|------|------|------|------|------|------|------|------|------|------|------|------|
| R/W | Reset Value Description                                                             |
| PMU_SOC_WAKEUP_INT_CLR       | 0    |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
| PMU_SOC_SLEEP_REJECT_INT_CLR | 0    |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
| PMU_SW_INT_CLR               | 0    |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
| PMU_SDIO_IDLE_INT_CLR        | 0    |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |
| PMU_LP_CPU_EXC_INT_CLR       | 0    |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |      |

PMU_OP1A_CNT_TARGETO_REACH_O_HP_INT_CLR   Write     1        to       clear
    PMU_OP1A_CNT_TARGETO_REACH_O_INT. (WT)

PMU_OP1A_CNT_TARGET1_REACH_O_HP_INT_CLR   Write     1        to       clear
    PMU_OP1A_CNT_TARGET1_REACH_O_INT. (WT)

PMU_OP1A_CNT_TARGETO_REACH_1_HP_INT_CLR    Write     1        to       clear
    PMU_OP1A_CNT_TARGETO_REACH_1_INT. (WT)

PMU_OP1A_CNT_TARGET1_REACH_1_HP_INT_CLR    Write     1        to       clear
    PMU_OP1A_CNT_TARGET1_REACH_1_INT. (WT)

PMU_OP2A_CNT_TARGETO_REACH_O_HP_INT_CLR    Write     1        to       clear
    VPMU_OP2A_CNT_TARGETO_REACH_O_INT. (WT)

PMU_OP2A_CNT_TARGET1_REACH_O_HP_INT_CLR    Write     1        to       clear
    PMU_OP2A_CNT_TARGET1_REACH_O_INT. (WT)

PMU_OP2A_CNT_TARGETO_REACH_1_HP_INT_CLR    Write     1        to       clear
    PMU_OP2A_CNT_TARGETO_REACH_1_INT. (WT)

PMU_OP2A_CNT_TARGET1_REACH_1_HP_INT_CLR    Write     1        to       clear
    PMU_OP2A_CNT_TARGET1_REACH_1_INT. (WT)

PMU_LP_CPU_EXC_INT_CLR                  Write 1 to clear PMU_LP_CPU_EXC_INT. (WT)
PMU_SDIO_IDLE_INT_CLR                   Write 1 to clear PMU_SDIO_IDLE_INT. (WT)
PMU_SW_INT_CLR                          Write 1 to clear PMU_SW_INT. (WT)
PMU_SOC_SLEEP_REJECT_INT_CLR            Write 1 to clear PMU_SOC_SLEEP_REJECT_INT. (WT)
PMU_SOC_WAKEUP_INT_CLR                  Write 1 to clear PMU_SOC_WAKEUP_INT. (WT)

```
```plaintext
Espressif Systems          1038          ESP32-P4 TRM
Submit Documentation Feedback        PRELIMINARY
```