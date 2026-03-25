

```markdown
|Priority Level|Event|
|:---------------|:---------------------|
|6|UTEA|
|7 (lowest)|UTEZ|

Table 36.3-4. Timing Events Priority when PWM Timer Decrementes
|Priority level|Event|
|:----------------------|:-------------------------------|
|1 (highest)|Software-forced event|
|2|DTEZ|
|3|DTO|
|4|DT1|
|5|DTEB|
|6|DTEA|
|7 (lowest)|DTEP|

Notes:

1. UTEP and UTEZ do not happen simultaneously. When the PWM timer is in count-up mode, UTEP will always happen one cycle earlier than UTEZ, as demonstrated in Figure 36.3-11, so their action on PWM signals will not interrupt each other. When the PWM timer is in count-up-down mode, UTEP will not occur.
2. DTEP and DTEZ do not happen simultaneously. When the PWM timer is in count-down mode, DTEZ will always happen one cycle earlier than DTEP, as demonstrated in Figure 36.3-12, so their action on PWM signals will not interrupt each other. When the PWM timer is in count-up-down mode, DTEZ will not occur.

PWM Signal Generation

The PWM generator module controls the behavior of outputting PWMxA and PWMxB when a particular timing event occurs. The timing events are further qualified by the PWM timer’s counting mode (increment or decrement). Knowing the counting mode, the module may then perform an independent action at each stage of the PWM timer counting up or down.

The following actions may be configured on PWMxA and PWMxB outputs:

*   Set High: Set the output of PWMxA or PWMxB to a high level
*   Clear Low: Clear the output of PWMxA or PWMxB by setting it to a low level
*   Toggle: Change the current output level of PWMxA or PWMxB to the opposite value. If it is currently pulled up, then pull it down, or vice versa.
*   Do Nothing: Keep both outputs PWMxA and PWMxB unchanged. In this state, interrupts can still be triggered.

Actions on outputs are configured by using registers MCPWM_GENx_A_REG and MCPWM_GENx_B_REG. So, the action to be taken on each output is set independently. Also, there is great flexibility in selecting actions to be taken on a given output based on events. More specifically, any event listed in Table 36.3-2 can operate on either output of PWMxA or PWMxB. To check out registers for particular generators 0, 1, or 2, please refer to register descriptions in Section 36.4.
```