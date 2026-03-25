

```markdown
B. Bit 1 to 10 of the configuration data is used to configure the number of times the counter overflows per an increase or decrease of Lpointn (hereafter referred to as LEDC_CHn_GAMMA_DUTY_CYCLE). In other words, Lpointn will increase or decrease after the counter overflows for the configured number of times.

C. Bit 11 to 20 of the configuration data is used to configure the amount by which Lpointn increase or decrease in the current configured range (hereafter referred to as LEDC_CHn_GAMMA_SCALE).

D. Bit 21 to 30 of the configuration data is used to configure the number of fades in the current configured range (hereafter referred to as LEDC_CHn_GAMMA_DUTY_NUM).

E. The duty cycle range number (from 0 to 15) specifies to which range the above configuration data apply. For gamma curve fading, it must start from 0 and increase by 1 for the next range to be configured.

F. Once the above procedures are finished, the configuration for one range is complete.

Other ranges are configured by repeating the same set of procedures. You can configure any number of ranges from 0 to 15, and each can be configured independently.

iv. After all required ranges are configured, write the total number of ranges configured in Step 3 to the LEDC_CHn_GAMMA_ENTRY_NUM field of the LEDC_CHn_GAMMA_CONF_REG register.

v. Set the LEDC_PARA_UP_CHn field to apply the above configuration. After this field is set, the configurations for duty cycle fading will take effect upon the next overflow of the counter, and the PWM generator will output a gamma curve fading PWM signal following the configurations. LEDC_PARA_UP_CHn field will be automatically cleared by hardware.

After the above procedures, the LED PWM controller will generate the desired PWM signals.

At any time, duty cycle fading can be suspended or resumed, more details can be found in section 40.4.3.3. If the duty cycle fading configurations need to be changed before the PWM signals stop fading (that is, the LEDC_DUTY_CHNG_END_CHn_INT has not been triggered), the duty cycle fading needs to be suspended before changing the configurations. However, if the duty cycle fading configurations need to be changed after the PWM signals stop fading (that is, the LEDC_DUTY_CHNG_END_CHn_INT has been triggered), the configurations can be changed directly.

At any time, PWM signal output can be enabled or disabled by software, and the output signal level can be changed, more details can be found in section 40.4.2.
```

## 40.8 Memory Blocks

Each LEDC channel has a memory to store duty cycle fading configuration data. Each memory can store configuration data for up to 16 ranges. The addresses in this section are relative to LED PWM Controller base address provided in Table 6.3-2 in Chapter 6 System and Memory.

Table 40.8-1. LEDC Memory Blocks

| Name                  | Description           | Size   | Starting Address         | Ending Address                     | Access |
|-----------------------|-----------------------|--------|--------------------------|------------------------------------|--------|
| LEDC_CHn_MEM          | Memory of PWMn        | 64 B   | 0x400 + PWMn * 64       | 0x400 + (PWMn + 1) * 64            | R/W    |
```