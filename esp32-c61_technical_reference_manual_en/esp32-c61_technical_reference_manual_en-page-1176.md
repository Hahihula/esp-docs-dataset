

```markdown
Register 31.6. LEDC_CHn_GAMMA_CONF_REG (n: 0-5) (0x0100+0x4*n)

| Bit | Name                                 | Description                                                                 |
|-----|---------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                           |                                                                             |
| 7   | LEDC_CHn_GAMMA_ENTRY_NUM             | Configures the number of duty cycle fading ranges for LEDC channel n. (R/W)    |
| 6   | LEDC_CHn_GAMMA_PAUSE                 | Configures whether to pause duty cycle fading of LEDC channel n.<br>0: Invalid. No effect<br>1: Pause (WT) |
| 5   | LEDC_CHn_GAMMA_RESUME                | Configures whether to resume duty cycle fading of LEDC channel n.<br>0: Invalid. No effect<br>1: Resume (WT) |
| 4   | LEDC_CHn_GAMMA_GAMMA_PAUSE           |                                                                             |
| 3   | LEDC_CHn_GAMMA_GAMMA_RESUME          |                                                                             |
| 2   | LEDC_CHn_GAMMA_GAMMA_ENTRY_NUM       |                                                                             |
| 1   | Reset                                | 0x0                                                                            |
```