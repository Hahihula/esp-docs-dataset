

```markdown
(d) Configure the `LEDC_CHn_GAMMA_DUTY_NUM` field of the `LEDC_CHn_GAMMA_WR_REG` register for the currently configured range.

(e) Write the duty cycle range number (from 0 to 15) to the `LEDC_CHn_GAMMA_WR_ADDR` field of the `LEDC_CHn_GAMMA_WR_ADDR_REG` register. This range number specifies to which range the above configurations apply. It must start from 0 and increase by 1 for the next range to be configured.

(f) Once the above procedures are finished, the configuration for one range is complete. Other ranges are configured by repeating the same set of procedures. You can configure any number of ranges from 0 to 16, and each can be configured independently.

4. After all required ranges are configured, write the total number of ranges configured in Step 3 to the `LEDC_CHn_GAMMA_ENTRY_NUM` field of the `LEDC_CHn_GAMMA_CONF_REG` register.

5. Set the `LEDC_PARA_UP_CHn` field to apply the above configuration. After this field is set, the configurations for duty cycle fading will take effect upon the next overflow of the counter, and the PWM generator will output a gamma curve fading PWM signal following the configurations. The `LEDC_PARA_UP_CHn` field will be automatically cleared by hardware.

After the above procedures, the PWM generator can generate a PWM signal with

`LEDC_CHn_GAMMA_ENTRY_NUM` ranges. The duty cycle of the PWM signal fades according to the configurations of range 0 first, and then range 1, till range (`LEDC_CHn_GAMMA_ENTRY_NUM - 1`) (the last range) where Duty Cycle Fading ends. The PWM signal fades independently in each range. In range `LEDC_CHn_GAMMA_WR_ADDR`, every time when the counter overflows for

`LEDC_CHn_GAMMA_DUTY_CYCLE` times, Lpointn increases or decreases (configured by `LEDC_CHn_GAMMA_DUTY_INC`) by `LEDC_CHn_GAMMA_SCALE`, and accordingly the duty cycle increases or decreases (configured by `LEDC_CHn_GAMMA_DUTY_INC`) by

```markdown
    LEDC_CHn_GAMMA_SCALE
-------------------------
    LEDC_TIMERx_DUTY_RES
```

After the duty cycle fades for `LEDC_CHn_GAMMA_DUTY_NUM` times in a range, Duty Cycle Fading in this range finishes.

When Duty Cycle Fading finishes in all ranges (the number of ranges is specified by `LEDC_CHn_GAMMA_ENTRY_NUM`), the PWM signal stops fading and keeps the duty cycle of the last fade.

Given that the duty cycle fades differently and linearly in each range, several linear fading ranges would be fitted to a gamma curve.

Figure 35.3-6 illustrates a gamma curve fading PWM signal.
```