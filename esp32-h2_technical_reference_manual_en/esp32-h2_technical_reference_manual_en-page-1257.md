

```markdown
Register 40.16. APB_SARADC_DMA_CONF_REG (0x0050)

APB_SARADC_APB_ADC_EOF_NUM Configures the number of samples. When the sampling reaches the configured number, the EOF flag bit sent to GDMA will be pulled high.
(R/W)

APB_SARADC_APB_ADC_RESET FSM Configures whether to reset DIG ADC controller status.
O: No effect
1: Reset
(R/W)

APB_SARADC_APB_ADC_TRANS Configures whether to let DIG ADC controller use GDMA.
O: No effect
1: DIG ADC controller uses DMA
(R/W)

Register 40.17. APB_SARADC_CTRL_DATE_REG (0x03FC)

APB_SARADC_DATE Version control register for SAR ADC and the temperature sensor. (R/W)
```