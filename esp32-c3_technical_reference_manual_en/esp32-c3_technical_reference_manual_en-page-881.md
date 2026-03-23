

```markdown
Register 34.4. APB_SARADC_SAR_PATT_TAB1_REG (0x0018)

APB_SARADC_SAR_PATT_TAB1 Pattern table entries 0 ~ 3 (each entry is six bits). (R/W)


Register 34.5. APB_SARADC_SAR_PATT_TAB2_REG (0x001C)

APB_SARADC_SAR_PATT_TAB2 Pattern table entries 4 ~ 7 (each entry is six bits). (R/W)


Register 34.6. APB_SARADC_ONETIME_SAMPLE_REG (0x0020)
```

```markdown
| Bit | Description |
|-----|-------------|
| 31  | reserved    |
| 30  | APB_SARADC1_ONETIME_SAMPLE |
| 29  | APB_SARADC2_ONETIME_SAMPLE |
| 28  | APB_SARADC_ONETIME_START   |
| 27  | APB_SARADC_ONETIME_CHANNEL |
| 26  | APB_SARADC_ONETIME_ATTEN   |
| 25  | reserved                  |
| 24  | reserved                  |
| 23  | reserved                  |
| ... | ...                       |
| 13  | reserved                  |
| 12  | reserved                  |
| 11  | reserved                  |
| 10  | reserved                  |
| 9   | reserved                  |
| 8   | reserved                  |
| 7   | reserved                  |
| 6   | reserved                  |
| 5   | reserved                  |
| 4   | reserved                  |
| 3   | reserved                  |
| 2   | reserved                  |
| 1   | reserved                  |
| 0   | reserved                  |

APB_SARADC_ONETIME_ATTEN Configure the attenuation for a one-time sampling. (R/W)
APB_SARADC_ONETIME_CHANNEL Configure the channel for a one-time sampling. (R/W)
APB_SARADC_ONETIME_START Start SAR ADC one-time sampling. (R/W)
APB_SARADC2_ONETIME_SAMPLE Enable SAR ADC2 one-time sampling. (R/W)
APB_SARADC1_ONETIME_SAMPLE Enable SAR ADC1 one-time sampling. (R/W)
```