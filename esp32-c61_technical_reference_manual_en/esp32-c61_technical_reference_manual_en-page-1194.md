

```markdown
Register 32.4. APB_TSENS_SAMPLE_REG (0x0068)

APB_SARADC_TSENS_SAMPLE_RATE Configures the sampling rate for hardware-triggered automatic temperature monitoring. The sampling period = configured value × the sensor's working clock cycle. (R/W)

APB_SARADC_TSENS_SAMPLE_EN Configures whether to enable automatic temperature monitoring.
O: Disable
1: Enable
(R/W)

Register 32.5. APB_SARADC_CTRL_DATE_REG (0x03FC)

APB_SARADC_DATE Version control register for SAR ADC (please refer to Chapter 33 ADC Controller for more information) and the temperature sensor. (R/W)
```