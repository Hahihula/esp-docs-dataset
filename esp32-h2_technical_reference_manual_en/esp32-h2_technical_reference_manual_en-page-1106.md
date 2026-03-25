
```markdown
Register 36.14. MCPWM_TIMER_SYNCI_CFG_REG (0x0034)

| Bit | Field Name                                 | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | O                                         | Reset                                                                       |
| 29  | O                                         | Reset                                                                       |
| 28  | O                                         | Reset                                                                       |
| 27  | O                                         | Reset                                                                       |
| 26  | O                                         | Reset                                                                       |
| 25  | O                                         | Reset                                                                       |
| 24  | O                                         | Reset                                                                       |
| 23  | MCPWM_TIMER0_SYNCISEL                     | Configures sync input for PWM timer0:<br>1: PWM timer0 sync out<br>2: PWM timer1 sync out<br>3: PWM timer2 sync out<br>4: SYNC0 from GPIO matrix<br>5: SYNC1 from GPIO matrix<br>6: SYNC2 from GPIO matrix<br>Other values: no sync input selected (R/W) |
| 22  | MCPWM_TIMER1_SYNCISEL                     | Configures sync input for PWM timer1:<br>1: PWM timer0 sync out<br>2: PWM timer1 sync out<br>3: PWM timer2 sync out<br>4: SYNC0 from GPIO matrix<br>5: SYNC1 from GPIO matrix<br>6: SYNC2 from GPIO matrix<br>Other values: no sync input selected (R/W) |
| 21  | MCPWM_TIMER2_SYNCISEL                     | Configures sync input for PWM timer2:<br>1: PWM timer0 sync out<br>2: PWM timer1 sync out<br>3: PWM timer2 sync out<br>4: SYNC0 from GPIO matrix<br>5: SYNC1 from GPIO matrix<br>6: SYNC2 from GPIO matrix<br>Other values: no sync input selected (R/W) |
| 20  | MCPWM_EXTERNAL_SYNCIO_INVERT              | Inverts SYNC0 from GPIO matrix. (R/W)                                     |
| 19  | MCPWM_EXTERNAL_SYNCI1_INVERT              | Inverts SYNC1 from GPIO matrix. (R/W)                                     |
| 18  | MCPWM_EXTERNAL_SYNCI2_INVERT              | Inverts SYNC2 from GPIO matrix. (R/W)                                     |
```