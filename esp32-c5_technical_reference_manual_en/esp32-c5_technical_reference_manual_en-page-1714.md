

```markdown
| Name                                       | Description                                                                 | Address | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|--------|
| **Configuration Registers**                |                                                                             |         |        |
| APB_SARADC_CTRL_REG                        | SAR ADC control register 1                                                  | 0x0000  | R/W    |
| APB_SARADC_CTRL2_REG                       | SAR ADC control register 2                                                  | 0x0004  | R/W    |
| APB_SARADC_FILTER_CTRL1_REG                | Filtering control register 1                                                | 0x0008  | R/W    |
| APB_SARADC_SAR_PATT_TAB1_REG               | Pattern table register 1                                                    | 0x0018  | R/W    |
| APB_SARADC_SAR_PATT_TAB2_REG               | Pattern table register 2                                                    | 0x001C  | R/W    |
| APB_SARADC_ONETIME_SAMPLE_REG              | Configuration register for one-shot sampling                               | 0x0020  | R/W    |
| APB_SARADC_FILTER_CTRL0_REG                | Filtering control register 0                                                | 0x0028  | R/W    |
| APB_SARADC_SAR1DATA_STATUS_REG             | SAR ADC conversion data storage register                                    | 0x002C  | RO     |
| APB_SARADC_THRESO_CTRL_REG                 | Filtered data threshold control register O                                 | 0x0034  | R/W    |
| APB_SARADC_THRESH1_CTRL_REG                | Filtered data threshold control register 1                                 | 0x0038  | R/W    |
| APB_SARADC_THRESH_CTRL_REG                 | Filtered data threshold control register                                   | 0x003C  | R/W    |
| APB_SARADC_INT_ENA_REG                     | Enable register of SAR ADC interrupts                                      | 0x0040  | R/W    |
| APB_SARADC_INT_RAW_REG                     | Raw register of SAR ADC interrupts                                         | 0x0044  | R/WTC/SS|
| APB_SARADC_INT_ST_REG                      | State register of SAR ADC interrupts                                       | 0x0048  | RO     |
| APB_SARADC_INT_CLR_REG                     | Clear register of SAR ADC interrupts                                       | 0x004C  | WT     |
| APB_SARADC_DMA_CONF_REG                    | DMA configuration register for SAR ADC                                    | 0x0050  | R/W    |
| APB_SARADC_CTRL_DATE_REG                   | Version control register                                                   | 0x03FC  | R/W    |
```