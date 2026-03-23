

```markdown
- Wait for a while and then read the data from `APB_SARADC_TSENS_OUT`. The output value gradually approaches the actual temperature linearly as the measurement time increases.

The actual temperature (°C) can be obtained by converting the output of temperature sensor via the following formula:

$$T(^\circ C) = 0.4386 \times VALUE - 27.88 \times offset - 20.52$$

VALUE in the formula is the output of the temperature sensor, and the offset is determined by the temperature offset. The temperature offset varies in different actual environment (the temperature range). For details, refer to Table 34.3-1.

Table 34.3-1. Temperature Offset
| Measurement Range (°C) | Temperature Offset (°C) |
|------------------------|-------------------------|
| 50 ~ 125               | -2                      |
| 20 ~ 100               | -1                      |
| -10 ~ 80               | 0                       |
| -30 ~ 50               | 1                       |
| -40 ~ 20               | 2                       |

## 34.4 Interrupts

- `APB_SARADC_ADC1_DONE_INT`: Triggered when SAR ADC1 completes one data conversion.
- `APB_SARADC_ADC2_DONE_INT`: Triggered when SAR ADC2 completes one data conversion.
- `APB_SARADC_THRESx_HIGH_INT`: Triggered when the sampling value is higher than the high threshold of monitor x.
- `APB_SARADC_THRESx_LOW_INT`: Triggered when the sampling value is lower than the low threshold of monitor x.

## 34.5 Register Summary

The addresses in this section are relative to the ADC controller base address provided in Table 3.3-3 in Chapter 3 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| **Configuration Registers** | | | |
| `APB_SARADC_CTRL_REG` | SAR ADC control register 1 | 0x0000 | R/W |
| `APB_SARADC_CTRL2_REG` | SAR ADC control register 2 | 0x0004 | R/W |
| `APB_SARADC_FILTER_CTRL1_REG` | Filtering control register 1 | 0x0008 | R/W |
| `APB_SARADC_SAR_PATT_TAB1_REG` | Pattern table register 1 | 0x0018 | R/W |
| `APB_SARADC_SAR_PATT_TAB2_REG` | Pattern table register 2 | 0x001C | R/W |
| `APB_SARADC_ONETIME_SAMPLE_REG` | Configuration register for one-time sampling | 0x0020 | R/W |
```