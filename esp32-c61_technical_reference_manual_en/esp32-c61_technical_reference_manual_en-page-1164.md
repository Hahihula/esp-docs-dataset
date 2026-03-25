

```markdown
Chapter 31 LED PWM Controller (LEDC)

After the procedures, the PWM generator can generate a PWM signal with `LEDC_CHn_GAMMA_ENTRY_NUM` ranges. The duty cycle of the PWM signal fades according to the configurations of range 0 first, and then range 1, till range (`LEDC_CHn_GAMMA_ENTRY_NUM - 1`) (the last range) where Duty Cycle Fading ends. The PWM signal fades independently in each range. According to the configuration of each range, every time when the counter overflows for `LEDC_CHn_GAMMA_DUTY_CYCLE` times, Lpoint increases or decreases (configured by `LEDC_CHn_GAMMA_DUTY_INC`) by `LEDC_CHn_GAMMA_SCALE`, and accordingly the duty cycle increases or decreases (configured by `LEDC_CHn_GAMMA_DUTY_INC`) by

```markdown
LEDC_CHn_GAMMA_SCALE / LEDC_TIMERx_DUTY_RES
```

After the duty cycle fades for `LEDC_CHn_GAMMA_DUTY_NUM` times in a range, Duty Cycle Fading in this range finishes.

When Duty Cycle Fading finishes in all ranges (the number of ranges is specified by `LEDC_CHn_GAMMA_ENTRY_NUM`), the PWM signal stops fading and keeps the duty cycle of the last fade.

Given that the duty cycle fades differently and linearly in each range, several linear fading ranges would be fitted to a gamma curve.

Figure 31.4-5 illustrates a gamma curve fading PWM signal.

![Figure 31.4-5 Output Signal of Gamma Curve Fading](image)

Figure 31.4-5. Output Signal of Gamma Curve Fading

31.4.3.3 Suspend and Resume Duty Cycle Fading

To suspend Duty Cycle Fading that has already been started, write 1 to the `LEDC_CHn_GAMMA_PAUSE` field of the `LEDC_CHn_GAMMA_CONF_REG` register. Once `LEDC_CHn_GAMMA_PAUSE` is set to 1, the PWM signal keeps the duty cycle of the most recent fade.

To resume Duty Cycle Fading, write 1 to the `LEDC_CHn_GAMMA_RESUME` field of the `LEDC_CHn_GAMMA_CONF_REG` register. Once `LEDC_CHn_GAMMA_RESUME` is set to 1, the PWM signal resumes fading from the range where the suspension occurs, until fading in the last range finishes. The fading will continue from the state when it was paused until all the ranges complete duty cycle fading (when
```