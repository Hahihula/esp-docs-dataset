

```markdown
| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | SOC_ETM_GDMA_AHB_EVT_OUT_FIFO_FULL_CH1_ST                                    |
| 30  | SOC_ETM_GDMA_AHB_EVT_OUT_FIFO_FULL_CH0_ST                                   |
| 29  | SOC_ETM_GDMA_AHB_EVT_OUT_FIFO_EMPTY_CH2_ST                                  |
| 28  | SOC_ETM_GDMA_AHB_EVT_OUT_FIFO_EMPTY_CH1_ST                                  |
| 27  | SOC_ETM_GDMA_AHB_EVT_OUT_TOTL_CH0_ST                                        |
| 26  | SOC_ETM_GDMA_AHB_EVT_OUT_TOTL_CH1_ST                                        |
| 25  | SOC_ETM_GDMA_AHB_EVT_OUT_EOF_CH0_ST                                         |
| 24  | SOC_ETM_GDMA_AHB_EVT_OUT_EOF_CH1_ST                                         |
| 23  | SOC_ETM_GDMA_AHB_EVT_OUT_EOF_CH2_ST                                         |
| 22  | SOC_ETM_GDMA_AHB_EVT_OUT_EOF_CH0_ST                                         |
| 21  | SOC_ETM_GDMA_AHB_EVT_OUT_EOF_CH1_ST                                         |
| 20  | SOC_ETM_GDMA_AHB_EVT_OUT_EOF_CH2_ST                                         |
| 19  | SOC_ETM_GDMA_AHB_EVT_OUT_DONE_CH0_ST                                        |
| 18  | SOC_ETM_GDMA_AHB_EVT_OUT_DONE_CH1_ST                                        |
| 17  | SOC_ETM_GDMA_AHB_EVT_OUT_DONE_CH2_ST                                        |
| 16  | SOC_ETM_GDMA_AHB_EVT_IN_DONE_CH0_ST                                         |
| 15  | SOC_ETM_GDMA_AHB_EVT_IN_DONE_CH1_ST                                         |
| 14  | SOC_ETM_GDMA_AHB_EVT_IN_DONE_CH2_ST                                         |
| 13  | SOC_ETM_GDMA_AHB_EVT_IN_FULL_CH0_ST                                         |
| 12  | SOC_ETM_GDMA_AHB_EVT_IN_FULL_CH1_ST                                         |
| 11  | SOC_ETM_GDMA_AHB_EVT_IN_FULL_CH2_ST                                         |
| 10  | SOC_ETM_GDMA_AHB_EVT_IN_EOF_CH0_ST                                          |
| 9   | SOC_ETM_GDMA_AHB_EVT_IN_EOF_CH1_ST                                          |
| 8   | SOC_ETM_GDMA_AHB_EVT_IN_EOF_CH2_ST                                          |
| 7   | SOC_ETM_GDMA_AHB_EVT_IN_EMPTY_CH0_ST                                        |
| 6   | SOC_ETM_GDMA_AHB_EVT_IN_EMPTY_CH1_ST                                        |
| 5   | SOC_ETM_GDMA_AHB_EVT_IN_EMPTY_CH2_ST                                        |
| 4   | SOC_ETM_ULP_EVT_ERR_INTR_ST                                                 |
| 3   | SOC_ETM_ULP_EVT_HALT_ST                                                     |
| 2   | SOC_ETM_ULP_EVT_START_INTR_ST                                               |
| 1   | SOC_ETM_RTC_EVT_TICK_ST                                                     |
| 0   | Reset                                                                       |

SOC_ETM_ULP_EVT_ERR_INTR_ST Represents the status of ULP_EVT_ERR_INTR.
O: Not received
1: Received
(R/WTC/SS)

SOC_ETM_ULP_EVT_HALT_ST Represents the status of ULP_EVT_HALT.
O: Not received
1: Received
(R/WTC/SS)

SOC_ETM_ULP_EVT_START_INTR_ST Represents the status of ULP_EVT_START_INTR.
O: Not received
1: Received
(R/WTC/SS)

SOC_ETM_RTC_EVT_TICK_ST Represents the status of RTC_EVT_TICK.
O: Not received
1: Received
(R/WTC/SS)

SOC_ETM_RTC_EVT_OVF_ST Represents the status of RTC_EVT_OVF.
O: Not received
1: Received
(R/WTC/SS)

SOC_ETM_RTC_EVT_CMP_ST Represents the status of RTC_EVT_CMP.
O: Not received
1: Received
(R/WTC/SS)
```