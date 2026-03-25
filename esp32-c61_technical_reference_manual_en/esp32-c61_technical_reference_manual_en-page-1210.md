

```markdown
Register 33.6. APB_SARADC_ONETIME_SAMPLE_REG (0x0020)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | APB_SARADC_ONETIME_SAMPLE (reserved)                                       |
| 30  | APB_SARADC_ONETIME_START                                                   |
| 29  | APB_SARADC_ONETIME_CHANNEL                                                 |
| 28  | APB_SARADC_ONETIME_ATTEN                                                   |
| 27  | (reserved)                                                                 |
| 26  | (reserved)                                                                 |
| 25  | (reserved)                                                                 |
| 24  | (reserved)                                                                 |
| 23  | (reserved)                                                                 |
| 22  | (reserved)                                                                 |
| ... | ...                                                                        |
| 13  | 0                                                                           |
| 12  | 0                                                                           |
| 11  | 0                                                                           |
| 10  | 0                                                                           |
| 9   | 0                                                                           |
| 8   | 0                                                                           |
| 7   | 0                                                                           |
| 6   | 0                                                                           |
| 5   | 0                                                                           |
| 4   | 0                                                                           |
| 3   | 0                                                                           |
| 2   | 0                                                                           |
| 1   | 0                                                                           |
| 0   | Reset                                                                      |

APB_SARADC_ONETIME_ATTEN Configures the attenuation for a one-shot sampling.
- 0: 0 dB
- 1: 2.5 dB
- 2: 6 dB
- 3: 12 dB
(R/W)

APB_SARADC_ONETIME_CHANNEL Configures the channel for a one-shot sampling.
- 0: Channel 0
- 1: Channel 1
- 2: Channel 2
- 3: Channel 3
(R/W)

APB_SARADC_ONETIME_START Configures whether to start SAR ADC one-shot sampling.
- 0: No effect
- 1: Start
(R/W)

APB_SARADC_ONETIME_SAMPLE Configures whether to enable SAR ADC one-shot sampling.
- 0: Disable
- 1: Enable
(R/W)
```