

```markdown
Register 46.6. APB_SARADC_ONETIME_SAMPLE_REG (0x0020)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | ... | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|-----|---|
|     | 0  | 0  | 13 | 0  | 0  | 0  | 0  | 0  | 0  | 0  | ... | 0 |
| Reset |    |    |    |    |    |    |    |    |    |    |     |   |

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
- 4: Channel 4
- 5: Channel 5
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