

```markdown
Chapter 33 ADC Controller

GoBack

• k: the filter coefficient

The filters are configured as follows:
• Configure APB_SARADC_FILTER_CHANNELx to select the ADC channel for filter x (x=0, 1).
• Configure APB_SARADC_FILTER_FACTORx to set the coefficient k for filter x.

33.5.10 Threshold Monitors

Two threshold monitors are available in the DIG ADC controller to monitor the filtered data in multi-channel sampling mode. When the data is above the high threshold, a high threshold interrupt is triggered; when the data is below the low threshold, a low threshold interrupt is triggered. Both monitors can be configured to any ADC channel, but cannot be configured to the same channel.

Threshold monitors are configured as follows:
• Set APB_SARADC_THRESx_EN to enable threshold monitor x (x=0, 1).
• Configure APB_SARADC_THRESx_LOW to set a low threshold.
• Configure APB_SARADC_THRESx_HIGH to set a high threshold.
• Configure APB_SARADC_THRESx_CHANNEL to select the channel to monitor.
• Set APB_SARADC_THRES_ALL_EN to enable threshold monitoring functionality.

33.5.11 GDMA Support

As SAR ADC has only one data register APB_SARADC_DATA for storing converted result from one-shot sampling, it is necessary to enable GDMA when converting data on multiple channels so that the data can be transferred to memory continuously.

GDMA support is triggered by the timer in the DIG ADC controller. Users can switch the DMA data path to the DIG ADC controller by configuring APB_SARADC_APB_ADC_TRANS. For specific DMA configuration, please refer to Chapter 3 GDMA Controller (GDMA).

GDMA Data Format

The ADC eventually passes 32-bit data to GDMA. The data format is shown in Figure 33.5-8.

Figure 33.5-8. DMA Data Format

data 12-bit ADC conversion result
ch_sel 3-bit channel information

Espressif Systems          1202         ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```