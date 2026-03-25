

```markdown
| Signal     | Event Description                                                                 | PWM Timer Operation |
|------------|-------------------------------------------------------------------------------------|---------------------|
| DTEP       | PWM timer value is equal to the period register value                              |                     |
| DTEZ       | PWM timer value is equal to zero                                                   |                     |
| DTEA       | PWM timer value is equal to register A                                             | PWM timer counts down |
| DTEB       | PWM timer value is equal to register B                                             |                     |
| DTO event  | Based on fault or synchronization events                                           |                     |
| DT1 event   | Based on fault or synchronization events                                           |                     |
| UTEP       | PWM timer value is equal to the period register value                              |                     |
| UTEZ       | PWM timer value is equal to zero                                                   |                     |
| UTEA       | PWM timer value is equal to register A                                             | PWM timer counts up |
| UTEB       | PWM timer value is equal to register B                                             |                     |
| UTO event   | Based on fault or synchronization events                                           |                     |
| UT1 event   | Based on fault or synchronization events                                           |                     |
| Software-force event | Software-initiated asynchronous event                                          | N/A                 |
```

Table 36.3-2. Timing Events Used in PWM Generator

The purpose of a software-force event is to impose non-continuous or continuous changes on the `PWMxA` and `PWMxB` outputs. The change is done asynchronously. Software-force control is handled by the `MCPWM_GENx_FORCE_REG` register.

The selection and configuration of TO/T1 in the PWM generator module are independent of the configuration of fault events in the fault handler module. A particular trip event may or may not be configured to cause trip action in the fault handler submodule, but the same event can be used by the PWM generator to trigger TO/T1 for controlling PWM waveforms.

It is important to know that when the PWM timer is in count-up-down mode, it will always decrement after a TEP event, and increment after a TEZ event. So, when the PWM timer is in count-up-down mode, DTEP and UTEZ events will occur, while UTEP and DTEZ events will never occur.

The PWM generator can handle multiple events at the same time. Events are prioritized by the hardware and relevant details are provided in Table 36.3-3 and Table 36.3-4. Priority levels range from 1 (the highest) to 7 (the lowest). Please note that the priority of TEP and TEZ events depends on the PWM timer’s counting mode.

If the value of A or B is set to be greater than the period, then U/DTEA and U/DTEB will never occur.

Table 36.3-3. Timing Events Priority When PWM Timer Increments

| Priority Level | Event                  |
|----------------|------------------------|
| 1 (highest)    | Software-forced event  |
| 2              | UTEP                   |
| 3              | UTO                    |
| 4              | UT1                    |
| 5              | UTEB                   |
```