

```markdown
Register 12.5. SOC_ETM_EVT_ST2_REG (0x0188)

| Bit | Name                                                                 | Description                                                                                                                                 |
|-----|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 31  | SOC_ETM_ADC_EVT_STOPPEDO_ST                                          | Represents ADC_EVT_STOPPEDO trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                               |
| 30  | SOC_ETM_ADC_EVT_RESULT_DONEO_ST                                       | Represents ADC_EVT_RESULT_DONEO trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 29  | SOC_ETM_ADC_EVT_EQ_BELOW_THRESH1_ST                                  | Represents ADC_EVT_EQ_BELOW_THRESH1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                         |
| 28  | SOC_ETM_ADC_EVT_EQ_ABOVE_THRESH1_ST                                  | Represents ADC_EVT_EQ_ABOVE_THRESH1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                         |
| 27  | SOC_ETM_MCPWM0_EVT_OP1_TE1_ST                                        | Represents MCPWM0_EVT_OP1_TE1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                               |
| 26  | SOC_ETM_MCPWM0_EVT_OP1_TE2_ST                                        | Represents MCPWM0_EVT_OP1_TE2 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                               |
| 25  | SOC_ETM_MCPWM0_EVT_OP2_TE1_ST                                        | Represents MCPWM0_EVT_OP2_TE1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                               |
| 24  | SOC_ETM_MCPWM0_EVT_OP2_TE2_ST                                        | Represents MCPWM0_EVT_OP2_TE2 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                               |
| 23  | SOC_ETM_MCPWM0_EVT_CAP1_ST                                           | Represents MCPWM0_EVT_CAP1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                               |
| 22  | SOC_ETM_MCPWM0_EVT_CAP2_ST                                           | Represents MCPWM0_EVT_CAP2 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                               |
| 21  | SOC_ETM_MCPWM0_EVT_FO_ST                                             | Represents MCPWM0_EVT_FO trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                                 |
| 20  | SOC_ETM_MCPWM0_EVT_F1_ST                                             | Represents MCPWM0_EVT_F1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                                 |
| 19  | SOC_ETM_MCPWM0_EVT_TZ1_OST_ST                                        | Represents MCPWM0_EVT_TZ1_OST trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 18  | SOC_ETM_MCPWM0_EVT_TZ2_OST_ST                                        | Represents MCPWM0_EVT_TZ2_OST trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 17  | SOC_ETM_MCPWM0_EVT_F2_CBC_ST                                         | Represents MCPWM0_EVT_F2_CBC trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 16  | SOC_ETM_MCPWM0_EVT_FL_CLR_ST                                        | Represents MCPWM0_EVT_FL_CLR trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 15  | SOC_ETM_MCPWM0_EVT_FO_TEB_ST                                         | Represents MCPWM0_EVT_FO_TEB trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 14  | SOC_ETM_MCPWM0_EVT_OP2_TE1_ST                                       | Represents MCPWM0_EVT_OP2_TE1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 13  | SOC_ETM_MCPWM0_EVT_OP2_TE2_ST                                       | Represents MCPWM0_EVT_OP2_TE2 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 12  | SOC_ETM_MCPWM0_EVT_FO_ST                                             | Represents MCPWM0_EVT_FO trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                                 |
| 11  | SOC_ETM_MCPWM0_EVT_F1_ST                                             | Represents MCPWM0_EVT_F1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                                 |
| 10  | SOC_ETM_MCPWM0_EVT_TZ1_OST_ST                                        | Represents MCPWM0_EVT_TZ1_OST trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 9   | SOC_ETM_MCPWM0_EVT_TZ2_OST_ST                                        | Represents MCPWM0_EVT_TZ2_OST trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 8   | SOC_ETM_MCPWM0_EVT_F2_CBC_ST                                         | Represents MCPWM0_EVT_F2_CBC trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 7   | SOC_ETM_MCPWM0_EVT_FL_CLR_ST                                        | Represents MCPWM0_EVT_FL_CLR trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 6   | SOC_ETM_MCPWM0_EVT_FO_TEB_ST                                         | Represents MCPWM0_EVT_FO_TEB trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 5   | SOC_ETM_MCPWM0_EVT_OP2_TE1_ST                                       | Represents MCPWM0_EVT_OP2_TE1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 4   | SOC_ETM_MCPWM0_EVT_OP2_TE2_ST                                       | Represents MCPWM0_EVT_OP2_TE2 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 3   | SOC_ETM_MCPWM0_EVT_FO_ST                                             | Represents MCPWM0_EVT_FO trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                                 |
| 2   | SOC_ETM_MCPWM0_EVT_F1_ST                                             | Represents MCPWM0_EVT_F1 trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                                 |
| 1   | SOC_ETM_MCPWM0_EVT_TZ1_OST_ST                                        | Represents MCPWM0_EVT_TZ1_OST trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |
| 0   | SOC_ETM_MCPWM0_EVT_TZ2_OST_ST                                        | Represents MCPWM0_EVT_TZ2_OST trigger status.<br>0: Not triggered<br>1: Triggered (R/WTC/SS)                                             |

SOC_ETM_MCPWM0_EVT_OP2_TEA_ST  Represents MCPWM0_EVT_OP2_TEA trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_MCPWM0_EVT_OPO_TEB_ST  Represents MCPWM0_EVT_OPO_TEB trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_MCPWM0_EVT_OP1_TEB_ST  Represents MCPWM0_EVT_OP1_TEB trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_MCPWM0_EVT_OP2_TEB_ST  Represents MCPWM0_EVT_OP2_TEB trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_MCPWM0_EVT_FO_ST  Represents MCPWM0_EVT_FO trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

SOC_ETM_MCPWM0_EVT_F1_ST  Represents MCPWM0_EVT_F1 trigger status.
O: Not triggered
1: Triggered
(R/WTC/SS)

Continued on the next page...
```