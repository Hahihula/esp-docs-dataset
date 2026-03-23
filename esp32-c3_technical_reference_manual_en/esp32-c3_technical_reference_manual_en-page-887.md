

```markdown
Chapter 34 On-Chip Sensor and Analog Signal Processing

Register 34.17. APB_SARADC_INT_CLR_REG (0x004C)

APB_SARADC_THRES1_LOW_INT_CLR Clear bit of APB_SARADC_THRES1_LOW_INT interrupt. (WO)
APB_SARADC_THRESO_LOW_INT_CLR Clear bit of APB_SARADC_THRESO_LOW_INT interrupt. (WO)
APB_SARADC_THRES1_HIGH_INT_CLR Clear bit of APB_SARADC_THRES1_HIGH_INT interrupt. (WO)
APB_SARADC_THRESO_HIGH_INT_CLR Clear bit of APB_SARADC_THRESO_HIGH_INT interrupt. (WO)
APB_SARADC_ADC2_DONE_INT_CLR Clear bit of APB_SARADC_ADC2_DONE_INT interrupt. (WO)
APB_SARADC_ADC1_DONE_INT_CLR Clear bit of APB_SARADC_ADC1_DONE_INT interrupt. (WO)

Register 34.18. APB_SARADC_DMA_CONF_REG (0x0050)

APB_SARADC_APB_ADC_EOF_NUM Generate dma_in_suc_eof when sample cnt = eof_num. (R/W)
APB_SARADC_APB_ADC_RESET_FSM Reset DIG ADC controller status. (R/W)
APB_SARADC_APB_ADC_TRANS When this bit is set, DIG ADC controller uses DMA. (R/W)
```