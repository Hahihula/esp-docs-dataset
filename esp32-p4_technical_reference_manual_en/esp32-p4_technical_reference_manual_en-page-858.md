

```markdown
Register 13.7. SOC_ETM_EVT_ST4_REG (0x01C8)

| Bit | Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | SOC_ETM_I2S2_EVT_X_WORDS_SENT_ST                                     | Separates the status of I2S2.                                                                                                             |
| 30  | SOC_ETM_I2S2_EVT_X_WORDS_RECEIVED_ST                                 |                                                                                                                                              |
| 29  | SOC_ETM_I2S2_EVT_TX_DONE_ST                                           |                                                                                                                                              |
| 28  | SOC_ETM_I2S1_EVT_RX_DONE_ST                                           |                                                                                                                                              |
| 27  | SOC_ETM_I2S1_EVT_X_WORDS_SENT_ST                                     |                                                                                                                                              |
| 26  | SOC_ETM_I2S1_EVT_X_WORDS_RECEIVED_ST                                 |                                                                                                                                              |
| 25  | SOC_ETM_I2S1_EVT_TX_DONE_ST                                           |                                                                                                                                              |
| 24  | SOC_ETM_I2S0_EVT_RX_DONE_ST                                           |                                                                                                                                              |
| 23  | SOC_ETM_I2S0_EVT_X_WORDS_SENT_ST                                     |                                                                                                                                              |
| 22  | SOC_ETM_I2S0_EVT_X_WORDS_RECEIVED_ST                                 |                                                                                                                                              |
| 21  | SOC_ETM_I2S0_EVT_TX_DONE_ST                                           |                                                                                                                                              |
| 20  | SOC_ETM_TWS_EVT_ST                                                    |                                                                                                                                              |
| 19  | SOC_ETM_TWS_EVT_RX_DONE_ST                                            |                                                                                                                                              |
| 18  | SOC_ETM_TWS_EVT_X_WORDS_SENT_ST                                      |                                                                                                                                              |
| 17  | SOC_ETM_TWS_EVT_X_WORDS_RECEIVED_ST                                  |                                                                                                                                              |
| 16  | SOC_ETM_TWS_EVT_TX_DONE_ST                                            |                                                                                                                                              |
| 15  | SOC_ETM_TPSNS_EVT_ST                                                  |                                                                                                                                              |
| 14  | SOC_ETM_REGDMA_EVT_OVER_ST                                           |                                                                                                                                              |
| 13  | SOC_ETM_REGDMA_EVT_LIMIT_ST                                          |                                                                                                                                              |
| 12  | SOC_ETM_REGDMA_ERR0_ST                                                |                                                                                                                                              |
| 11  | SOC_ETM_REGDMA_ERR1_ST                                                |                                                                                                                                              |
| 10  | SOC_ETM_REGDMA_ERR2_ST                                                |                                                                                                                                              |
| 9   | SOC_ETM_REGDMA_ERR3_ST                                                |                                                                                                                                              |
| 8   | SOC_ETM_REGDMA_EVT_DONE_ST                                            |                                                                                                                                              |
| 7   | SOC_ETM_ADC_AGC_EVT_DONE_ST                                           |                                                                                                                                              |
| 6   | SOC_ETM_ADC_AGC_EVT_STARTED_ST                                        |                                                                                                                                              |
| 5   | SOC_ETM_ADC_AGC_EVT_STOPPED_ST                                        |                                                                                                                                              |
| 4   | SOC_ETM_ADC_AGC_EVT_RESULT_DONE_ST                                    |                                                                                                                                              |
| 3   | SOC_ETM_ADC_AGC_EVT_RESULT_EQ_BELOW_THRESHO                          |                                                                                                                                              |
| 2   | SOC_ETM_ADC_AGC_EVT_RESULT_EQ_ABOVE_THRESH1                          |                                                                                                                                              |
| 1   | SOC_ETM_MCPWM1_EVT_OP0_TEE2_ST                                       | Represents the status of MCPWM1_EVT_OPO_TEE2.                                                                                               |
| 0   | SOC_ETM_MCPWM1_EVT_OPO_TEE2_ST                                       | Represents the status of MCPWM1_EVT_OPO_TEE2.                                                                                               |

SOC_ETM_MCPWM1_EVT_OPO_TEE2_ST
- 0: Not received
- 1: Received (R/WTC/SS)

SOC_ETM_MCPWM1_EVT_OP1_TEE2_ST
- 0: Not received
- 1: Received (R/WTC/SS)

SOC_ETM_MCPWM1_EVT_OP2_TEE2_ST
- 0: Not received
- 1: Received (R/WTC/SS)

SOC_ETM_ADC_EVT_CONV_CMPLTO_ST
- 0: Not received
- 1: Received (R/WTC/SS)

SOC_ETM_ADC_EVT_EQ_ABOVE_THRESHO_ST
- Represents the status of ADC_EVT_EQ_ABOVE_THRESHO.
- 0: Not received
- 1: Received (R/WTC/SS)

SOC_ETM_ADC_EVT_EQ_ABOVE_THRESH1_ST
- Represents the status of ADC_EVT_EQ_ABOVE_THRESH1.
- 0: Not received
- 1: Received (R/WTC/SS)
```