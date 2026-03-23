

```markdown
Register 39.16. APB_SARADC_DMA_CONF_REG (0x0050)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  |                                             |                                                                             |
| 30  | APB_SARADC_APB_ADC_EOF_NUM                 | Configures whether to enable generating dma_in_suc_eof when sample cnt = eof_num.<br>0: No effect<br>1: Generate (R/W) |
| 29  | APB_SARADC_APB_ADC_RESET_FSM               | Configures whether to reset DIG ADC controller status.<br>0: No effect<br>1: Reset (R/W) |
| 28  | APB_SARADC_APB_ADC_TRANS                   | Configures whether to let DIG ADC controller use DMA.<br>0: No effect<br>1: DIG ADC controller uses DMA (R/W) |
```