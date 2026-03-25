

```markdown
Register 46.3. APB_SARADC_FILTER_CTRL1_REG (0x0008)

APB_SARADC_FILTER_FACTOR1   Configures the filter coefficient k for SAR ADC filter 1.
O: k=0 (i.e., the filter is disabled)
1: k=2
2: k=4
3: k=8
4: k=16
5: k=32
6: k=64
(R/W)

APB_SARADC_FILTER_FACTOR0   Configures the filter coefficient k for SAR ADC filter 0 (same as above). (R/W)


Register 46.4. APB_SARADC_SAR_PATT_TAB1_REG (0x0018)

APB_SARADC_SAR_PATT_TAB1   Configures pattern 0 ~ 3 (each pattern takes six bits). For details see Section 46.5.8 Pattern Table. (R/W)
```