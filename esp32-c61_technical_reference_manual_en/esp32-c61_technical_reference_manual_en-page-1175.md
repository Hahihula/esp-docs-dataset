

```markdown
Register 31.4. LEDC_CHn_CONF1_REG (n: 0-5) (0x000C+0x14*n)

LEDC_DUTY_START_CHn Configures whether the duty cycle fading configurations take effect.
O: Not take effect
1: Take effect
(R/W/SC)
```

```markdown
Register 31.5. LEDC_TIMERx_CONF_REG (x: 0-3) (0x00A0+0x8*x)

LEDC_TIMERx_DUTY_RES Configures the bit width of the counter in timer x. Valid values are 1 to 20. (R/W)

LEDC_CLK_DIV_TIMERx Configures the divisor for the divider in timer x.
The least significant eight bits represent the fractional part. The most significant ten bits represent the integer part. (R/W)

LEDC_TIMERx_PAUSE Configures whether to pause the counter in timer x.
O: Normal
1: Pause
(R/W)

LEDC_TIMERx_RST Configures whether to reset timer x. The counter will show 0 after reset.
O: Not reset
1: Reset
(R/W)

LEDC_TIMERx_PARA_UP Configures whether to update LEDC_CLK_DIV_TIMERx and LEDC_TIMERx_DUTY_RES.
O: Invalid. No effect
1: Update
(WT)
```