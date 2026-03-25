

```markdown
| Bit | Field Name                                                                                   | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | (reserved)                                                                                  | -                                                                                                                                          |
| 30  | SOC_ETM_PMU_EVT_SLEEP_WAKEUP_ST_CLR                                                       | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_ST_CLR                                                                             |
| 29  | SOC_ETM_GDMA_EVT_OUT_FIFO_FULL_CH2_ST_CLR                                                 | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH0_ST_CLR                                                                     |
| 28  | SOC_ETM_GDMA_EVT_OUT_FIFO_FULL_CH1_ST_CLR                                                 | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH1_ST_CLR                                                                     |
| 27  | SOC_ETM_GDMA_EVT_OUT_FIFO_EMPTY_CH0_ST_CLR                                                | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH0_ST_CLR                                                                     |
| 26  | SOC_ETM_GDMA_EVT_OUT_FIFO_EMPTY_CH1_ST_CLR                                                | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH1_ST_CLR                                                                     |
| 25  | SOC_ETM_GDMA_EVT_OUT_TOTAL_EOF_CH0_ST_CLR                                                 | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH0_ST_CLR                                                                     |
| 24  | SOC_ETM_GDMA_EVT_OUT_TOTAL_EOF_CH1_ST_CLR                                                 | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH1_ST_CLR                                                                     |
| 23  | SOC_ETM_GDMA_EVT_OUT_TOTAL_EOF_CH2_ST_CLR                                                 | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH2_ST_CLR                                                                     |
| 22  | SOC_ETM_GDMA_EVT_OUT_EOF_CH0_ST_CLR                                                       | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH0_ST_CLR                                                                     |
| 21  | SOC_ETM_GDMA_EVT_OUT_EOF_CH1_ST_CLR                                                       | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH1_ST_CLR                                                                     |
| 20  | SOC_ETM_GDMA_EVT_OUT_EOF_CH2_ST_CLR                                                       | Configures whether or not to clear SOC_ETM_GDMA_EVT_OUT_DONE_CH2_ST_CLR                                                                     |
| 19  | SOC_ETM_GDMA_EVT_OUT_DONE_CH0_ST_CLR                                                      | Configures whether or not to clear GDMA_EVT_OUT_DONE_CH0 trigger status.                                                                    |
| 18  | SOC_ETM_GDMA_EVT_OUT_DONE_CH1_ST_CLR                                                      | Configures whether or not to clear GDMA_EVT_OUT_DONE_CH1 trigger status.                                                                    |
| 17  | SOC_ETM_GDMA_EVT_OUT_DONE_CH2_ST_CLR                                                      | Configures whether or not to clear GDMA_EVT_OUT_DONE_CH2 trigger status.                                                                    |
| 16  | Reset                                                                                       | -                                                                                                                                              |

SOC_ETM_GDMA_EVT_OUT_DONE_CHO_ST_CLR   Configures whether or not to clear GDMA_EVT_OUT_DONE_CHO trigger status.
O: Invalid. No effect
1: Clear
(WT)

SOC_ETM_GDMA_EVT_OUT_DONE_CH1_ST_CLR    Configures whether or not to clear GDMA_EVT_OUT_DONE_CH1 trigger status.
O: Invalid. No effect
1: Clear
(WT)

SOC_ETM_GDMA_EVT_OUT_DONE_CH2_ST_CLR    Configures whether or not to clear GDMA_EVT_OUT_DONE_CH2 trigger status.
O: Invalid. No effect
1: Clear
(WT)

SOC_ETM_GDMA_EVT_OUT_EOF_CHO_ST_CLR     Configures whether or not to clear GDMA_EVT_OUT_EOF_CHO trigger status.
O: Invalid. No effect
1: Clear
(WT)

SOC_ETM_GDMA_EVT_OUT_EOF_CH1_ST_CLR     Configures whether or not to clear GDMA_EVT_OUT_EOF_CH1 trigger status.
O: Invalid. No effect
1: Clear
(WT)
```