
```markdown
Chapter 40 LED PWM Controller (LEDC)

ii. Set the `LEDC_DUTY_START_CHn` field to enable Duty Cycle Fading. When this field is cleared, Duty Cycle Fading will be disabled.

iii. Write the linear duty cycle fading configuration to (`LEDC_CHn_MEM` starting address + duty cycle range number * 4), the `LEDC_CHn_MEM` starting address is provided in Table 40.8-1.
Please note that the following bit names are just for easier description, and there are no such register fields.

A. Bit 0 of the configuration data is used to configure the direction (hereafter referred to as `LEDC_CHn_GAMMA_DUTY_INC`). When it is set or cleared, the Lpointn will increase or decrease in the current configured range.

B. Bit 1 to 10 of the configuration data is used to configure the number of times the counter overflows per an increment or decrement of Lpointn (hereafter referred to as `LEDC_CHn_GAMMA_DUTY_CYCLE`). In other words, Lpointn will increase or decrease after the counter overflows for the configured number of times.

C. Bit 11 to 20 of the configuration data is used to configure the amount by which Lpointn increase or decrease in the current configured range (hereafter referred to as `LEDC_CHn_GAMMA_SCALE`).

D. Bit 21 to 30 of the configuration data is used to configure the number of fades in the current configured range (hereafter referred to as `LEDC_CHn_GAMMA_DUTY_NUM`).

E. The duty cycle range number (from 0 to 15) specifies to which range the above configuration data apply. For linear duty cycle fading only the first range needs to be configured, so the duty cycle range number should be configured as 0.

iv. Configure the number of ranges per each fading (1 in this case) via the `LEDC_CHn_GAMMA_ENTRY_NUM` field of the `LEDC_CHn_GAMMA_CONF_REG`. Once the specified number of ranges have been faded, Duty Cycle Fading stops and the PWM generator triggers the `LEDC_DUTY_CHNG_END_CHn_INT` interrupt. For linear duty cycle fading there is only one duty cycle range (i.e. the first one), so configure `LEDC_CHn_GAMMA_ENTRY_NUM` as 1.

v. Set the `LEDC_PARA_UP_CHn` field to apply the above configurations. After this field is set, the configurations for Duty Cycle Fading will take effect upon the next overflow of the counter, and the PWM generator will output a linear fading PWM signal following configurations. The `LEDC_PARA_UP_CHn` field will be automatically cleared by hardware.

(b) Gamma curve fading:

i. The same as Step 1 in Section 40.4.3.1.

ii. The same as Step 2 in Section 40.4.3.1.

iii. Configure multiple duty cycle ranges with the following steps. Write the gamma curve fading configuration to (`LEDC_CHn_MEM` starting address + duty cycle range number * 4), the `LEDC_CHn_MEM` starting address is provided in Table 40.8-1.

A. Bit 0 of the configuration data is used to configure the direction (hereafter referred to as `LEDC_CHn_GAMMA_DUTY_INC`). When it is set or cleared, the Lpointn will increment or decrement in the current configured range.
```