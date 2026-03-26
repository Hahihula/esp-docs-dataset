

```markdown
| Signal       | Event Description                                                                 | PWM Timer Operation |
|--------------|-------------------------------------------------------------------------------------|---------------------|
| DTEP         | PWM timer value is equal to the period register value                              |                     |
| DTEZ         | PWM timer value is equal to zero                                                   |                     |
| DTEA         | PWM timer value is equal to register A                                             | PWM timer counts down |
| DTB          | PWM timer value is equal to register B                                             |                     |
| DTO event    | Based on fault or synchronization events                                           |                     |
| DT1 event    | Based on fault or synchronization events                                           |                     |
| UTEP         | PWM timer value is equal to the period register value                              |                     |
| UTEZ         | PWM timer value is equal to zero                                                   |                     |
| UTEA         | PWM timer value is equal to register A                                             | PWM timer counts up |
| UTB          | PWM timer value is equal to register B                                             |                     |
| UTO event    | Based on fault or synchronization events                                           |                     |
| UT1 event    | Based on fault or synchronization events                                           |                     |
| Software-force event | Software-initiated asynchronous event                                          | N/A                 |

Table 56.3-2. Timing Events Used in PWM Generator
```