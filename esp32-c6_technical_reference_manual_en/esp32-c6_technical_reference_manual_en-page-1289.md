

```markdown
Register 36.70. MCPWM_INT_RAW_REG (0x0114)

| Bit | Name                         | Description                                                                 |
|-----|------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                     |                                                                             |
| 30  | MCPWM_CAP2_INT_RAW           | Represents the raw status for the interrupt triggered when the timer O stops. (R/WTC/SS) |
| 29  | MCPWM_CAP1_INT_RAW           | Represents the raw status for the interrupt triggered when the timer 1 stops. (R/WTC/SS) |
| 28  | MCPWM_CAP0_INT_RAW           | Represents the raw status for the interrupt triggered when the timer 2 stops. (R/WTC/SS) |
| 27  | MCPWM_TZ1_OST_INT_RAW        | Represents the raw status for the interrupt triggered by a PWM timer O TEZ event. (R/WTC/SS) |
| 26  | MCPWM_TZ1_CBC_INT_RAW        | Represents the raw status for the interrupt triggered by a PWM timer 1 TEZ event. (R/WTC/SS) |
| 25  | MCPWM_TZ2_OST_INT_RAW        | Represents the raw status for the interrupt triggered by a PWM timer 2 TEZ event. (R/WTC/SS) |
| 24  | MCPWM_TZ2_CBC_INT_RAW        | Represents the raw status for the interrupt triggered by a PWM timer O TEP event. (R/WTC/SS) |
| 23  | MCPWM_CMPR2_TE1_INT_RAW      | Represents the raw status for the interrupt triggered by a PWM timer 1 TEP event. (R/WTC/SS) |
| 22  | MCPWM_CMPR2_TE2_INT_RAW      | Represents the raw status for the interrupt triggered by a PWM timer 2 TEP event. (R/WTC/SS) |
| 21  | MCPWM_FAULT0_CLR_INT_RAW     | Represents the raw status for the interrupt triggered when fault_event0 ends. (R/WTC/SS) |
| 20  | MCPWM_FAULT1_CLR_INT_RAW     | Represents the raw status for the interrupt triggered when fault_event1 ends. (R/WTC/SS) |
| 19  | MCPWM_FAULT2_CLR_INT_RAW     |                                                                             |
| 18  | MCPWM_TIMER0_STOP_INT_RAW    | Represents the raw status for the interrupt triggered when the timer O stops. (R/WTC/SS) |
| 17  | MCPWM_TIMER1_STOP_INT_RAW    | Represents the raw status for the interrupt triggered when the timer 1 stops. (R/WTC/SS) |
| 16  | MCPWM_TIMER2_STOP_INT_RAW    | Represents the raw status for the interrupt triggered when the timer 2 stops. (R/WTC/SS) |
| 15  | MCPWM_TIMER0_TEZ_INT_RAW     | Represents the raw status for the interrupt triggered by a PWM timer O TEZ event. (R/WTC/SS) |
| 14  | MCPWM_TIMER1_TEZ_INT_RAW     | Represents the raw status for the interrupt triggered by a PWM timer 1 TEZ event. (R/WTC/SS) |
| 13  | MCPWM_TIMER2_TEZ_INT_RAW     | Represents the raw status for the interrupt triggered by a PWM timer 2 TEZ event. (R/WTC/SS) |
| 12  | MCPWM_TIMER0_TEP_INT_RAW     | Represents the raw status for the interrupt triggered by a PWM timer O TEP event. (R/WTC/SS) |
| 11  | MCPWM_TIMER1_TEP_INT_RAW     | Represents the raw status for the interrupt triggered by a PWM timer 1 TEP event. (R/WTC/SS) |
| 10  | MCPWM_TIMER2_TEP_INT_RAW     | Represents the raw status for the interrupt triggered by a PWM timer 2 TEP event. (R/WTC/SS) |
| 9   | MCPWM_FAULT0_INT_RAW         | Represents the raw status for the interrupt triggered when fault_event0 starts. (R/WTC/SS) |
| 8   | MCPWM_FAULT1_INT_RAW         | Represents the raw status for the interrupt triggered when fault_event1 starts. (R/WTC/SS) |
| 7   | MCPWM_FAULT2_INT_RAW         | Represents the raw status for the interrupt triggered when fault_event2 starts. (R/WTC/SS) |
| 6   | Reserved                     |                                                                             |
| 5   | Reserved                     |                                                                             |
| 4   | Reserved                     |                                                                             |
| 3   | Reserved                     |                                                                             |
| 2   | Reserved                     |                                                                             |
| 1   | Reserved                     |                                                                             |
| 0   | Reset                        |                                                                             |

Continued on the next page...
```