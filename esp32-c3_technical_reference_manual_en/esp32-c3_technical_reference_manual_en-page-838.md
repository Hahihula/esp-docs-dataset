

```markdown
Register 32.4. LEDC_CHn_HPOINT_REG (n: 0-5) (0x0004+20*n)

LEDC_HPOINT_CHn The output value changes to high when the selected timer for this channel has reached the value specified by this field. (R/W)


Register 32.5. LEDC_CHn_DUTY_REG (n: 0-5) (0x0008+20*n)

LEDC_DUTY_CHn This field is used to change the output duty by controlling the Lpoint. The output value turns to low when the selected timer for this channel has reached the Lpoint. (R/W)


Register 32.6. LEDC_CHn_DUTY_R_REG (n: 0-5) (0x0010+20*n)

LEDC_DUTY_R_CHn This field stores the current duty cycle of the output signal on channel n. (RO)
```