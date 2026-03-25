

```markdown
Register 33.16. APB_SARADC_DMA_CONF_REG (0x0050)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | APB_SARADC_APB_ADC_TRAN                                                   |
| 30  | APB_SARADC_APB_ADC_RESET FSM                                              |
|     |                                                                             |
| 29  |                                                                             |
| ... | (reserved)                                                                  |
| 16  |                                                                             |
| 15  |                                                                             |
| 0   | APB_SARADC_APB_ADC_EOF_NUM                                                 |

APB_SARADC_APB_ADC_EOF_NUM Configures the number of samples. When the sampling reaches the configured number, the EOF flag bit sent to GDMA will be pulled high. (R/W)

APB_SARADC_APB_ADC_RESET_FSM Configures whether to reset DIG ADC controller status.
- 0: No effect
- 1: Reset
(R/W)

APB_SARADC_APB_ADC_TRAN Configures whether to let DIG ADC controller use GDMA.
- 0: No effect
- 1: DIG ADC controller uses DMA
(R/W)
```