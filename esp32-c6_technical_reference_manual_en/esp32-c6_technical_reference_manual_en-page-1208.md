

```markdown
Chapter 36 Motor Control PWM (MCPWM)

Waveforms for Common Configurations

Figure 36.3-15 presents the symmetric PWM waveform generated when the PWM timer is in Count-Up-Down mode. DC 0%–100% modulation can be calculated via the formula below:

Duty = (Period − A) ÷ Period

If A matches the PWM timer value and the PWM timer is incrementing, then the PWM output is pulled up. If A matches the PWM timer value while the PWM timer is decrementing, then the PWM output is pulled low.

Figure 36.3-15. Symmetrical Waveform in Count-Up-Down Mode

The PWM waveforms in Figures 36.3-16 to 36.3-19 show some common PWM operator configurations. The following conventions are used in the figures:

* Period A and B refer to the values written in the corresponding registers.
* PWMxA and PWMxB are the output signals of PWM Operator x.
```