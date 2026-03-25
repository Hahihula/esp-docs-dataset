

```markdown
Register 12.11. SOC_ETM_TASK_ST3_REG (0x01E8)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----:|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|-----------------------------|
| 0   |    | SOC_ETM_LADC_TASK_STOP_O_ST (reserved) | SOC_ETM_LADC_TASK_START_O_ST (reserved) | SOC_ETM_LADC_TASK_SAMPLE_O_ST | SOC_ETM_MCPWMO_TASK_CAP2_ST | SOC_ETM_MCPWMO_TASK_CAP1_ST | SOC_ETM_MCPWMO_TASK_CAP0_ST | SOC_ETM_MCPWMO_TASK_CLRO_ST | SOC_ETM_MCPWMO_TASK_CLRU_ST | SOC_ETM_MCPWMO_TASK_CLRL_ST | SOC_ETM_MCPWMO_TASK_CLRO_ST | SOC_ETM_MCPWMO_TASK_TZ2_O_ST | SOC_ETM_MCPWMO_TASK_TZ1_O_ST | SOC_ETM_MCPWMO_TASK_TZO_O_ST | SOC_ETM_MCPWMO_TASK_TIMER2_PERIOD_UP_ST | SOC_ETM_MCPWMO_TASK_TIMER1_PERIOD_UP_ST | SOC_ETM_MCPWMO_TASK_TIMER2_PERIOD_UP_ST | SOC_ETM_MCPWMO_TASK_TIMER1_PERIOD_UP_ST | Reset |

SOC_ETM_TG1_TASK_ALARM_START_TIMER1_ST Represents TG1_TASK_ALARM_START_TIMER1 trigger status.
O: Not triggered
1: Triggered (R/WTC/SS)

SOC_ETM_TG1_TASK_CNT_STOP_TIMER1_ST Represents TG1_TASK_CNT_STOP_TIMER1 trigger status.
O: Not triggered
1: Triggered (R/WTC/SS)

SOC_ETM_TG1_TASK_CNT_RELOAD_TIMER1_ST Represents TG1_TASK_CNT_RELOAD_TIMER1 trigger status.
O: Not triggered
1: Triggered (R/WTC/SS)

SOC_ETM_TG1_TASK_CNT_CAP_TIMER1_ST Represents TG1_TASK_CNT_CAP_TIMER1 trigger status.
O: Not triggered
1: Triggered (R/WTC/SS)

SOC_ETM_MCPWMO_TASK_CMPRO_A_UP_ST Represents MCPWMO_TASK_CMPRO_A_UP trigger status.
O: Not triggered
1: Triggered (R/WTC/SS)
```