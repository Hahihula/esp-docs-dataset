

```markdown
Register 36.72. MCPWM_INT_CLR_REG (0x01C)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | MCPWM_CAP2_INT_CLR                   | Write 1 to clear MCPWM_CAP2_INT.                                            |
| 29  | MCPWM_CAP1_INT_CLR                   | Write 1 to clear MCPWM_CAP1_INT.                                            |
| 28  | MCPWM_CAP0_INT_CLR                   | Write 1 to clear MCPWM_CAP0_INT.                                            |
| 27  | MCPWM_TZ_OST_INT_CLR                 | Write 1 to clear MCPWM_TZ_OST_INT.                                          |
| 26  | MCPWM_TZO_CBC_INT_CLR                | Write 1 to clear MCPWM_TZO_CBC_INT.                                        |
| 25  | MCPWM_TZI_TZ7_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ7_INT.                                        |
| 24  | MCPWM_TZI_TZ6_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ6_INT.                                        |
| 23  | MCPWM_TZI_TZ5_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ5_INT.                                        |
| 22  | MCPWM_TZI_TZ4_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ4_INT.                                        |
| 21  | MCPWM_TZI_TZ3_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ3_INT.                                        |
| 20  | MCPWM_TZI_TZ2_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ2_INT.                                        |
| 19  | MCPWM_TZI_TZ1_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ1_INT.                                        |
| 18  | MCPWM_TZI_TZ0_INT_CLR                | Write 1 to clear MCPWM_TZI_TZ0_INT.                                        |
| 17  | MCPWM_CMPRO2_TEB_INT_CLR             | Write 1 to clear MCPWM_CMPRO2_TEB_INT.                                     |
| 16  | MCPWM_CMPR1_TEA_INT_CLR              | Write 1 to clear MCPWM_CMPR1_TEA_INT.                                      |
| 15  | MCPWM_CMPR0_TEA_INT_CLR              | Write 1 to clear MCPWM_CMPR0_TEA_INT.                                      |
| 14  | MCPWM_FAULT2_INT_CLR                 | Write 1 to clear MCPWM_FAULT2_INT.                                         |
| 13  | MCPWM_FAULT1_INT_CLR                 | Write 1 to clear MCPWM_FAULT1_INT.                                         |
| 12  | MCPWM_FAULT0_INT_CLR                 | Write 1 to clear MCPWM_FAULT0_INT.                                         |
| 11  | MCPWM_TIMER2_STOP_INT_CLR            | Write 1 to clear MCPWM_TIMER2_STOP_INT. (WT)                               |
| 10  | MCPWM_TIMER1_STOP_INT_CLR            | Write 1 to clear MCPWM_TIMER1_STOP_INT. (WT)                               |
| 9   | MCPWM_TIMER0_STOP_INT_CLR            | Write 1 to clear MCPWM_TIMER0_STOP_INT. (WT)                               |
| 8   | MCPWM_TIMER2_TEZ_INT_CLR             | Write 1 to clear MCPWM_TIMER2_TEZ_INT. (WT)                                |
| 7   | MCPWM_TIMER1_TEZ_INT_CLR             | Write 1 to clear MCPWM_TIMER1_TEZ_INT. (WT)                                |
| 6   | MCPWM_TIMER0_TEZ_INT_CLR             | Write 1 to clear MCPWM_TIMER0_TEZ_INT. (WT)                                |
| 5   | MCPWM_TIMER2_TEP_INT_CLR             | Write 1 to clear MCPWM_TIMER2_TEP_INT. (WT)                                |
| 4   | MCPWM_TIMER1_TEP_INT_CLR             | Write 1 to clear MCPWM_TIMER1_TEP_INT. (WT)                                |
| 3   | MCPWM_TIMER0_TEP_INT_CLR             | Write 1 to clear MCPWM_TIMER0_TEP_INT. (WT)                                |
| 2   | MCPWM_FAULT2_CLR_INT_CLR             | Write 1 to clear MCPWM_FAULT2_CLR_INT. (WT)                                |
| 1   | MCPWM_FAULT1_CLR_INT_CLR             | Write 1 to clear MCPWM_FAULT1_CLR_INT. (WT)                                |
| 0   | MCPWM_FAULT0_CLR_INT_CLR             | Write 1 to clear MCPWM_FAULT0_CLR_INT. (WT)                                |

MCPWM_TIMER0_STOP_INT_CLR    Write 1 to clear MCPWM_TIMER0_STOP_INT. (WT)
MCPWM_TIMER1_STOP_INT_CLR    Write 1 to clear MCPWM_TIMER1_STOP_INT. (WT)
MCPWM_TIMER2_STOP_INT_CLR    Write 1 to clear MCPWM_TIMER2_STOP_INT. (WT)

MCPWM_TIMER0_TEZ_INT_CLR     Write 1 to clear MCPWM_TIMER0_TEZ_INT. (WT)
MCPWM_TIMER1_TEZ_INT_CLR     Write 1 to clear MCPWM_TIMER1_TEZ_INT. (WT)
MCPWM_TIMER2_TEZ_INT_CLR     Write 1 to clear MCPWM_TIMER2_TEZ_INT. (WT)

MCPWM_TIMER0_TEP_INT_CLR     Write 1 to clear MCPWM_TIMER0_TEP_INT. (WT)
MCPWM_TIMER1_TEP_INT_CLR     Write 1 to clear MCPWM_TIMER1_TEP_INT. (WT)
MCPWM_TIMER2_TEP_INT_CLR     Write 1 to clear MCPWM_TIMER2_TEP_INT. (WT)

MCPWM_FAULT0_INT_CLR         Write 1 to clear MCPWM_FAULT0_INT. (WT)
MCPWM_FAULT1_INT_CLR         Write 1 to clear MCPWM_FAULT1_INT. (WT)
MCPWM_FAULT2_INT_CLR         Write 1 to clear MCPWM_FAULT2_INT. (WT)

MCPWM_FAULT0_CLR_INT_CLR     Write 1 to clear MCPWM_FAULT0_CLR_INT. (WT)
MCPWM_FAULT1_CLR_INT_CLR     Write 1 to clear MCPWM_FAULT1_CLR_INT. (WT)
MCPWM_FAULT2_CLR_INT_CLR     Write 1 to clear MCPWM_FAULT2_CLR_INT. (WT)

MCPWM_CMPRO_TEA_INT_CLR      Write 1 to clear MCPWM_CMPRO_TEA_INT. (WT)
MCPWM_CMPR1_TEA_INT_CLR      Write 1 to clear MCPWM_CMPR1_TEA_INT. (WT)
MCPWM_CMPR2_TEA_INT_CLR      Write 1 to clear MCPWM_CMPR2_TEA_INT. (WT)

MCPWM_CMPRO_TEB_INT_CLR      Write 1 to clear MCPWM_CMPRO_TEB_INT. (WT)
MCPWM_CMPR1_TEB_INT_CLR      Write 1 to clear MCPWM_CMPR1_TEB_INT. (WT)
MCPWM_CMPR2_TEB_INT_CLR      Write 1 to clear MCPWM_CMPR2_TEB_INT. (WT)

MCPWM_TZO_CBC_INT_CLR        Write 1 to clear MCPWM_TZO_CBC_INT. (WT)

Continued on the next page...
```