

```markdown
MCPWM_GENn_FORCE_REG registers.

The selection and configuration of T0/T1 in the PWM generator module is independent of the configuration of fault events in the fault handler module. A particular trip event may or may not be configured to cause trip action in the fault handler submodule, but the same event can be used by the PWM generator to trigger T0/T1 for controlling PWM waveforms.

It is important to know that when the PWM timer is in Count-Up-Down Mode, it will always decrement after a TEP event, and increment after a TEZ event. So, when the PWM timer is in Count-Up-Down Mode, DTEP and UTEZ events will occur, while UTEP and DTEZ events never occurs.

The PWM generator can handle multiple events at the same time. Events are prioritized by the hardware and relevant details are provided in Table 41.3-3 and Table 41.3-4. Priority levels range from 1 (the highest) to 7 (the lowest). Please note that the priority of TEP and TEZ events depends on the PWM timer’s counting mode.

If the value of A or B is set to be greater than the period, then U/DTEA and U/DTEB will never occur.

Table 41.3-3. Timing Events Priority When PWM Timer Increments

| Priority Level | Event             |
|----------------|-------------------|
| 1 (highest)    | Software-forced event |
| 2              | UTEP              |
| 3              | UTO               |
| 4              | UT1               |
| 5              | UTEB              |
| 6              | UTEA              |
| 7 (lowest)     | UTEZ              |

Table 41.3-4. Timing Events Priority when PWM Timer Decrements

| Priority level | Event             |
|----------------|-------------------|
| 1 (highest)    | Software-forced event |
| 2              | DTEZ              |
| 3              | DTO               |
| 4              | DT1               |
| 5              | DTEB              |
| 6              | DTEA              |
| 7 (lowest)     | DTEP              |

Notes:

1. UTEP and UTEZ do not happen simultaneously. When the PWM timer is in Count-Up Mode, UTEP will always happen one cycle earlier than UTEZ, as demonstrated in Figure 41.3-9, so their action on PWM signals will not interrupt each other. When the PWM timer is in Count-Up-Down Mode, UTEP will not occur.

2. DTEP and DTEZ do not happen simultaneously. When the PWM timer is in Count-Down Mode, DTEZ will always happen one cycle earlier than DTEP, as demonstrated in Figure 41.3-10, so their action on PWM
```