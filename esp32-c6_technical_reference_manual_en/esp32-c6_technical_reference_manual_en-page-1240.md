

```markdown
Chapter 36 Motor Control PWM (MCPWM) GoBack


Register 36.14. MCPWM_TIMER_SYNCI_CFG_REG (0x0034)


| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | O                                         | Reset                                                                       |
| 29  | O                                         | Reset                                                                       |
| 28  | O                                         | Reset                                                                       |
| 27  | O                                         | Reset                                                                       |
| 26  | O                                         | Reset                                                                       |
| 25  | O                                         | Reset                                                                       |
| 24  | O                                         | Reset                                                                       |
| 23  | MCPWM_TIMER0_SYNCISEL                     | Configures sync input for PWM timer0.                                     |
|     |                                            | 1: PWM timer0 sync out                                                       |
|     |                                            | 2: PWM timer1 sync out                                                       |
|     |                                            | 3: PWM timer2 sync out                                                       |
|     |                                            | 4: SYNC0 from GPIO matrix                                                    |
|     |                                            | 5: SYNC1 from GPIO matrix                                                    |
|     |                                            | 6: SYNC2 from GPIO matrix                                                    |
|     | Other values: no sync input selected      | (R/W)                                                                       |
| 22  | MCPWM_TIMER1_SYNCISEL                     | Select sync input for PWM timer1.                                          |
|     |                                            | 1: PWM timer0 sync out                                                       |
|     |                                            | 2: PWM timer1 sync out                                                       |
|     |                                            | 3: PWM timer2 sync out                                                       |
|     |                                            | 4: SYNC0 from GPIO matrix                                                    |
|     |                                            | 5: SYNC1 from GPIO matrix                                                    |
|     |                                            | 6: SYNC2 from GPIO matrix                                                    |
|     | Other values: no sync input selected      | (R/W)                                                                       |
| 21  | MCPWM_TIMER2_SYNCISEL                     | Select sync input for PWM timer2.                                          |
|     |                                            | 1: PWM timer0 sync out                                                       |
|     |                                            | 2: PWM timer1 sync out                                                       |
|     |                                            | 3: PWM timer2 sync out                                                       |
|     |                                            | 4: SYNC0 from GPIO matrix                                                    |
|     |                                            | 5: SYNC1 from GPIO matrix                                                    |
|     |                                            | 6: SYNC2 from GPIO matrix                                                    |
|     | Other values: no sync input selected      | (R/W)                                                                       |
| 20  | MCPWM_EXTERNAL_SYNCIO_INVERT              | Invert SYNC0 from GPIO matrix. (R/W)                                       |
| 19  | MCPWM_EXTERNAL_SYNCI1_INVERT              | Invert SYNC1 from GPIO matrix. (R/W)                                       |
| 18  | MCPWM_EXTERNAL_SYNCI2_INVERT              | Invert SYNC2 from GPIO matrix. (R/W)                                       |

Espressif Systems
1240
ESP32-C6 TRM (Version 1.1)
Submit Documentation Feedback
```