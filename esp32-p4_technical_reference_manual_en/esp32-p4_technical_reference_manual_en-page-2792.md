

```markdown
Register 55.6. LEDC_CHn_GAMMA_CONF_REG (n: 0-7) (0x0100+0x4*n)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | LEDC_CHn_GAMMA_ENTRY_NUM      | Configures the number of duty cycle fading ranges for LEDC channel n. (R/W)   |
| 29  | LEDC_CHn_GAMMA_PAUSE          | Configures whether to pause duty cycle fading of LEDC channel n.<br>0: Invalid. No effect<br>1: Pause (WT) |
| 28  | LEDC_CHn_GAMMA_RESUME         | Configures whether to resume duty cycle fading of LEDC channel n.<br>0: Invalid. No effect<br>1: Resume (WT) |
```