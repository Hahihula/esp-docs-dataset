

```markdown
| Priority Level | Event |
|:----------------|:-------|
| 3              | UTO    |
| 4              | UT1    |
| 5              | UTEB   |
| 6              | UTEA   |
| 7 (lowest)     | UTEZ   |

Table 56.3-4. Timing Events Priority when PWM Timer Decrements

| Priority level | Event                  |
|:---------------|:-----------------------|
| 1 (highest)    | Software-forced event  |
| 2              | DTEZ                   |
| 3              | DTO                    |
| 4              | DT1                    |
| 5              | DTEB                   |
| 6              | DTEA                   |
| 7 (lowest)     | DTEP                   |

Notes:

1. UTEP and UTEZ do not happen simultaneously. When the PWM timer is in Count-Up Mode, UTEP will always happen one cycle earlier than UTEZ, as demonstrated in Figure 56.3-9, so their action on PWM signals will not interrupt each other. When the PWM timer is in Count-Up-Down Mode, UTEP will not occur.

2. DTEP and DTEZ do not happen simultaneously. When the PWM timer is in Count-Down Mode, DTEZ will always happen one cycle earlier than DTEP, as demonstrated in Figure 56.3-10, so their action on PWM signals will not interrupt each other. When the PWM timer is in Count-Up-Down Mode, DTEZ will not occur.

PWM Signal Generation

The PWM generator module controls the behavior of outputting PWMxA and PWMxB when a particular timing event occurs. The timing events are further qualified by the PWM timer’s counting mode (increment or decrement). Knowing the counting mode, the module may then perform an independent action at each stage of the PWM timer counting up or down.

The following actions may be configured on PWMxA and PWMxB outputs:

*   Set High: Set the output of PWMxA or PWMxB to a high level.
*   Clear Low: Clear the output of PWMxA or PWMxB by setting it to a low level.
*   Toggle: Change the current output level of PWMxA or PWMxB to the opposite value. If it is currently pulled up, then pull it down, or vice versa.
*   Do Nothing: Keep both outputs PWMxA and PWMxB unchanged. In this state, interrupts can still be triggered.

Actions on outputs is configured by using registers MCPWM_GENn_A_REG and
```