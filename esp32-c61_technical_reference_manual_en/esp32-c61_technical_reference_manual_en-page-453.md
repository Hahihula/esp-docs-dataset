

```markdown
Register 10.10. SOC_ETM_TASK_ST3_REG (0x0EO)
| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    | SOC_ETM_GDMA_AHB_TASK_OUT_START_CHO_ST (reserved) | SOC_ETM_GDMA_AHB_TASK_IN_START_CH1_ST | SOC_ETM_GDMA_AHB_TASK_IN_START_ST | [Reserved] | 0 | SOC_ETM_I2SO_TASK_STOP_TX_ST | SOC_ETM_I2SO_TASK_STOP_RX_ST | SOC_ETM_I2SO_TASK_START_TX_ST | SOC_ETM_I2SO_TASK_START_RX_ST | SOC_ETM_TMPSNR_TASK_STOP_ST | (reserved) | SOC_ETM_ADC_TASK_STOP_O | SOC_ETM_ADC_TASK_SAMPLE_O | SOC_ETM_TG1_TASK_CNT_CAP_TIMER1_ST | Reset |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

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

SOC_ETM_ADC_TASK_SAMPLEO_ST Represents ADC_TASK_SAMPLEO trigger status.
O: Not triggered
1: Triggered (R/WTC/SS)
```
Continued on the next page...
```