
```markdown
## 62.8 Programming Procedure

### 62.8.1 HP ADC Multi-Channel Sampling Mode

The multi-channel sampling mode can be configured with the following procedure:

1. Set `PMU_XPD_PERIF_I2C` and `PMU_PERIF_I2C_RST` to power up HP ADC.
2. Configure `HP_SYS_CLKRST_ADC_CLK_SRC_SEL` to select HP ADC clock source.
3. Configure `HP_SYS_CLKRST_ADC_CLK_DIV_NUM` and `HP_SYS_CLKRST_ADC_SARx_CLK_DIV_NUM` to set clock division.
4. Set `HP_SYS_CLKRST_ADC_CLK_EN` to enable HP ADC clock.
5. Set `LPADC_SARx_DIG_FORCE` to enable the sampling channel.
6. Configure the pattern table as described in Section 62.5.6 HP ADC Pattern Table.
7. Configure channels and filtering coefficients as described in Section 62.5.9 HP ADC Filters.
8. Configure threshold monitoring as described in Section 62.5.10 HP ADC Threshold Monitors, as needed.
9. Set `ADC_APB_ADC_TRANS` to use GDMA.
10. Configure `ADC_TIMER_TARGET` to set trigger target for HP ADC timer.
11. Set `ADC_TIMER_EN` to enable the timer.

The timer timeout will trigger HP ADC FSM to start sampling according to the pattern table. The conversion result will be automatically stored in memory. When the sampling reaches the specified limit in `ADC_APB_ADC_EOF_NUM`, it will terminate.

Once sampling is complete, an `ADC_SARx_DONE_INT_RAW` interrupt will be generated.

### 62.8.2 LP ADC One-shot Sampling Mode

The one-shot sampling mode can be configured with the following procedure:

1. Set `PMU_XPD_PERIF_I2C` and `PMU_PERIF_I2C_RSTB` to power up LP ADC.
2. Configure `LPPERL_LPADC_FUNC_DIV_NUM` and `LPPERL_LPADC_SARx_DIV_NUM` to set the frequency of `LPADC_CLK` and `LPADCx_SARCLK`.
3. Configure `LPADC_SARx_EN_PAD` and `LPADC_SARx_ATTEN` to select sampling channels and attenuation.
4. Set `LPADC_SAR_MEASx_START_SAR` to enable the one-shot sampling mode of LP ADCx.

Once sampling is complete, an `LPADC_COCPU_SARADCx_INT_RAW` interrupt is generated. Software can read the conversion result from `LPADC_SAR_MEASn_DATA_SAR`.

### 62.8.3 LP ADC Automatic Monitoring

The configuration process for the automatic monitoring of the LP ADC controller is as follows:

1. Configure `LPADC_ADCx_HW_READ_RATE_I` to set the sampling rate.
2. Configure `LPADC_SARx_WAKEUP_MODE` to select the wake-up mode.
```