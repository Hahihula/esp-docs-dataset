

```markdown
Chapter 41 Motor Control PWM (MCPWM)    GoBack


Figure 41.3-8. Count-Up-Down Mode Waveforms, Count-Up at Synchronization Event



When the PWM timer is running, it generates the following timing events periodically and automatically:

*   UTEP: The timing event generated when the PWM timer’s value is equal to the value of the period field (MCPWM_TIMERn_PERIOD) and when the PWM timer is increasing.
*   UTEZ: The timing event generated when the PWM timer’s value equals zero and when the PWM timer is increasing.
*   DTEP: The timing event generated when the PWM timer’s value equals the value of the period field (MCPWM_TIMERn_PERIOD) and when the PWM timer is decreasing.
*   DTEZ: The timing event generated when the PWM timer’s value equals zero and when the PWM timer is decreasing.

Figures 41.3-9 to 41.3-11 show the timing waveforms of U/DTEP and U/DTEZ.
```