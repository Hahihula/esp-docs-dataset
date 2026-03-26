
```markdown
Chapter 62 ADC Controller (ADC)

Register 62.40. LPADC_SAR1_HW_WAKEUP_REG (0x006C)
| Bit 31 | Bit 17 | Bit 16 | Description                  |
|--------|--------|--------|-------------------------------|
|   0     |    0x64|    0   | Reset                         |

LPADC_ADC1_HW_READ_EN_I Configures whether to enable automatic monitoring for LP ADC1.
- 0: Disable
- 1: Enable
(R/W)

LPADC_ADC1_HW_READ_RATE_I Configures the sampling rate for hardware-triggered automatic monitoring for LP ADC1. The sampling period = configured value × LP ADC1’s working clock cycle. (R/W)


Register 62.41. LPADC_SAR2_HW_WAKEUP_REG (0x0070)
| Bit 31 | Bit 17 | Bit 16 | Description                  |
|--------|--------|--------|-------------------------------|
|   0     |    0x64|    0   | Reset                         |

LPADC_ADC2_HW_READ_EN_I Configures whether to enable automatic monitoring for LP ADC2.
- 0: Disable
- 1: Enable
(R/W)

LPADC_ADC2_HW_READ_RATE_I Configures the sampling rate for hardware-triggered automatic monitoring for LP ADC2. The sampling period = configured value × LP ADC2’s working clock cycle. (R/W)
```