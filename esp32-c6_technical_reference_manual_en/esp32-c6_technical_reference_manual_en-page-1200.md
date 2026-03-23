

```markdown
Chapter 36 Motor Control PWM (MCPWM)    GoBack

When the PWM timer is running, it generates the following timing events periodically and automatically:

* UTEP: The timing event generated when the PWM timer’s value is equal to the value of the period field (MCPWM_TIMERx_PERIOD) and when the PWM timer is increasing.
* UTEZ: The timing event generated when the PWM timer’s value equals to zero and when the PWM timer is increasing.
* DTEP: The timing event generated when the PWM timer’s value equals to the value of the period field (MCPWM_TIMERx_PERIOD) and when the PWM timer is decreasing.
* DTEZ: The timing event generated when the PWM timer’s value equals to zero and when the PWM timer is decreasing.

Figures 36.3-11 to 36.3-13 show the timing waveforms of U/DTEP and U/DTEZ.

Figure 36.3-11. UTEP and UTEZ Generation in Count-Up Mode
```