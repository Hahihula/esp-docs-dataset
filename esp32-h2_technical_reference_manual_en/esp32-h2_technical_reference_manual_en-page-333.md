

```markdown
Register 7.73. PCR_BUS_CLK_UPDATE_REG (0x0148)

PCR_BUS_CLOCK_UPDATE Configures whether or not to update configurations for CPU_CLK division, AHB_CLK division and HP_ROOT_CLK clock source selection.
- 0: Not update configurations
- 1: Update configurations
This bit is automatically cleared when configurations have been updated. (R/W/WTC)

Register 7.74. PCR_SAR_CLK_DIV_REG (0x014C)

PCR_SAR1_CLK_DIV_NUM Configures the divisor for SAR ADC clock to generate ADC analog control signals. (R/W)

Register 7.75. PCR_SYSCLK_FREQ_QUERY_O_REG (0x0120)

PCR_FOSC_FREQ Represents the frequency of RC_FAST_CLK.
Measurement unit: MHz.
(HRO)

PCR_PLL_FREQ Represents the frequency of PLL_F96M_CLK.
Measurement unit: MHz.
(HRO)
```