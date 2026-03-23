

```markdown
Register 36.72. MCPWM_INT_CLR_REG (0x01C)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 30  | MCPWM_CAP2_INT_CLR                   | Write 1 to clear the interrupt triggered when the timer 0 stops.            |
| 29  | MCPWM_CAP1_INT_CLR                   |                                                                             |
| 28  | MCPWM_CAP0_INT_CLR                   |                                                                             |
| 27  | MCPWM_OST_INT_CLR                    |                                                                             |
| 26  | MCPWM_TZ1_INT_CLR                    |                                                                             |
| 25  | MCPWM_TZ2_INT_CLR                    |                                                                             |
| 24  | MCPWM_CBC_INT_CLR                    |                                                                             |
| 23  | MCPWM_CMPR2_INT_CLR                  |                                                                             |
| 22  | MCPWM_CMPR1_INT_CLR                  |                                                                             |
| 21  | MCPWM_CMPRO2_TEP_INT_CLR             |                                                                             |
| 20  | MCPWM_CMPRO1_TEP_INT_CLR             |                                                                             |
| 19  | MCPWM_FAULT0_INT_CLR                 | Write 1 to clear the interrupt triggered when fault_event0 starts. (WT)     |
| 18  | MCPWM_FAULT1_INT_CLR                 | Write 1 to clear the interrupt triggered when fault_event1 starts. (WT)     |
| 17  | MCPWM_FAULT2_INT_CLR                 | Write 1 to clear the interrupt triggered when fault_event2 starts. (WT)     |
| 16  | MCPWM_TIMER0_STOP_INT_CLR            | Write 1 to clear the interrupt triggered when the timer 0 stops.            |
| 15  | MCPWM_TIMER1_STOP_INT_CLR            | Write 1 to clear the interrupt triggered when the timer 1 stops.            |
| 14  | MCPWM_TIMER2_STOP_INT_CLR            | Write 1 to clear the interrupt triggered when the timer 2 stops.            |
| 13  | MCPWM_TIMERO_TEZ_INT_CLR             | Write 1 to clear the interrupt triggered by a PWM timer 0 TEZ event. (WT)    |
| 12  | MCPWM_TIMER1_TEZ_INT_CLR             | Write 1 to clear the interrupt triggered by a PWM timer 1 TEZ event. (WT)    |
| 11  | MCPWM_TIMER2_TEZ_INT_CLR             | Write 1 to clear the interrupt triggered by a PWM timer 2 TEZ event. (WT)    |
| 10  | MCPWM_TIMERO_TEP_INT_CLR             | Write 1 to clear the interrupt triggered by a PWM timer 0 TEP event. (WT)    |
| 9   | MCPWM_TIMER1_TEP_INT_CLR             | Write 1 to clear the interrupt triggered by a PWM timer 1 TEP event. (WT)    |
| 8   | MCPWM_TIMER2_TEP_INT_CLR             | Write 1 to clear the interrupt triggered by a PWM timer 2 TEP event. (WT)    |
| 7   | MCPWM_FAULT0_INT_CLR                 |                                                                             |
| 6   | MCPWM_FAULT1_INT_CLR                 |                                                                             |
| 5   | MCPWM_FAULT2_INT_CLR                 |                                                                             |
| 4   | MCPWM_TIMER0_STOP_INT_CLR            |                                                                             |
| 3   | MCPWM_TIMER1_STOP_INT_CLR            |                                                                             |
| 2   | MCPWM_TIMER2_STOP_INT_CLR            |                                                                             |
| 1   | MCPWM_TIMERO_TEZ_INT_CLR             |                                                                             |
| 0   | MCPWM_TIMER1_TEZ_INT_CLR             |                                                                             |

Reset: All bits are cleared to 0.

MCPWM_TIMERO_STOP_INT_CLR Write 1 to clear the interrupt triggered when the timer 0 stops. (WT)
MCPWM_TIMER1_STOP_INT_CLR Write 1 to clear the interrupt triggered when the timer 1 stops. (WT)
MCPWM_TIMER2_STOP_INT_CLR Write 1 to clear the interrupt triggered when the timer 2 stops. (WT)
MCPWM_TIMERO_TEZ_INT_CLR Write 1 to clear the interrupt triggered by a PWM timer 0 TEZ event. (WT)
MCPWM_TIMER1_TEZ_INT_CLR Write 1 to clear the interrupt triggered by a PWM timer 1 TEZ event. (WT)
MCPWM_TIMER2_TEZ_INT_CLR Write 1 to clear the interrupt triggered by a PWM timer 2 TEZ event. (WT)
MCPWM_TIMERO_TEP_INT_CLR Write 1 to clear the interrupt triggered by a PWM timer 0 TEP event. (WT)
MCPWM_TIMER1_TEP_INT_CLR Write 1 to clear the interrupt triggered by a PWM timer 1 TEP event. (WT)
MCPWM_TIMER2_TEP_INT_CLR Write 1 to clear the interrupt triggered by a PWM timer 2 TEP event. (WT)
MCPWM_FAULT0_INT_CLR Write 1 to clear the interrupt triggered when fault_event0 starts. (WT)
MCPWM_FAULT1_INT_CLR Write 1 to clear the interrupt triggered when fault_event1 starts. (WT)
MCPWM_FAULT2_INT_CLR Write 1 to clear the interrupt triggered when fault_event2 starts. (WT)
MCPWM_FAULT0_INT_CLR Write 1 to clear the interrupt triggered when fault_event0 ends. (WT)

Continued on the next page...
```