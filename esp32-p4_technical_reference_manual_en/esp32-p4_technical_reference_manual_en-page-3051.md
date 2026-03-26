

```markdown
Register 62.24. LPADC_MEAS1_MUX_REG (0x0010)

LPADC_SAR1_DIG_FORCE                   (reserved)
31 30
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 Reset

LPADC_SAR1_DIG_FORCE   Configures whether to use HP ADC1 to control SAR ADC1.
0: SAR ADC1 controlled by LP ADC1 CTRL
1: SAR ADC1 controlled by HP ADC1 CTRL
(R/W)

Register 62.25. LPADC_ATTEN1_REG (0x0014)

LPADC_SAR1_ATTEN
31
0
Oxffffffff Reset

LPADC_SAR1_ATTEN   Configures the attenuation value for one-shot sampling of LP ADC1.
0: 0 dB
1: 2.5 dB
2: 6 dB
3: 12 dB
(R/W)
```