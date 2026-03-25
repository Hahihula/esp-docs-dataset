

```markdown
Register 31.1. LEDC_CHn_CONFO_REG (n: 0-5) (0x0000+0x14*n)

Continued from the previous page...

LEDC_OVF_CNT_RESET_CHn Configures whether to reset the ovf_cnt of channel n.
0: Invalid. No effect
1: Reset the ovf_cnt
(WT)

Register 31.2. LEDC_CHn_HPOINT_REG (n: 0-5) (0x0004+0x14*n)

LEDC_HPOINT_CHn Configures high point of signal output on channel n. The output value changes to high when the selected timers have reached the value specified by this register. (R/W)

Register 31.3. LEDC_CHn_DUTY_REG (n: 0-5) (0x0008+0x14*n)

LEDC_DUTY_CHn Configures the duty cycle of signal output on channel n. (R/W)
```