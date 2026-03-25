

```markdown
Note:
For definitions of interrupt, interrupt signal, interrupt source, and their correlations, please refer to Chapter 11 Interrupt Matrix > Section 11.2 Terminology.

Each interrupt source can be configured by a common set of registers that are described in Section Interrupt Configuration Registers. The specific registers can be found in Section 46.9 Register Summary.

## 46.8 Programming Procedure

### 46.8.1 Configuring One-shot Sampling Mode

The one-shot sampling mode can be configured with the following procedure:

1. Set PMU_XPD_PERIF_I2C and PMU_PERIF_I2C_RST to power up SAR ADC.
2. Configure `PCR_SARADC_CLKM_SEL` to select ADC clock source.
3. Configure `PCR_SARADC_CLKM_DIV_NUM` and `PCR_SAR1_CLK_DIV_NUM` to set clock division.
4. Set `PCR_SARADC_CLKM_EN` to enable ADC clock.
5. Set `APB_SARADC_ONETIME_SAMPLE` to enable the one-shot sampling mode.
6. Configure `APB_SARADC_ONETIME_CHANNEL` to select sampled channel.
7. Configure `APB_SARADC_ONETIME_ATTEN` to set attenuation as needed.
8. Set `APB_SARADC_ONETIME_START` to start one-shot sampling.

Once sampling is complete, an `APB_SARADC_ADC_DONE_IRQ` interrupt is generated. Software can read conversion result from `APB_SARADC_ADC_DATA`. To switch the sampled channel, program from step 6.

### 46.8.2 Configuring Multi-Channel Sampling Mode

The multi-channel sampling mode can be configured with the following procedure:

1. Set PMU_XPD_PERIF_I2C and PMU_PERIF_I2C_RST to power up SAR ADC.
2. Configure `PCR_SARADC_CLKM_SEL` to select ADC clock source.
3. Configure `PCR_SARADC_CLKM_DIV_NUM` and `PCR_SAR1_CLK_DIV_NUM` to set clock division.
4. Set `PCR_SARADC_CLKM_EN` to enable ADC clock.
5. Configure the pattern table as described in Section 46.5.8 Pattern Table.
6. Configure channels and filtering coefficients as described in Section 46.5.9 ADC Filters.
7. Configure threshold monitoring as described in Section 46.5.10 Threshold Monitors, as needed.
8. Set `APB_SARADC_APB_ADC_TRANS` to use GDMA.
9. Configure `APB_SARADC_TIMER_TARGET` to set trigger target for DIG ADC timer.
10. Set `APB_SARADC_TIMER_EN` to enable the timer.
```