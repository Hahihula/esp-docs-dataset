

```markdown
## Register 9.71. PCR_BUS_CLK_UPDATE_REG (0x0144)

PCR_BUS_CLOCK_UPDATE Configures whether or not to update configurations for CPU_CLK division, AHB_CLK division and HP_ROOT_CLK clock source selection.
- 0: Not update configurations
- 1: Update configurations

This bit is automatically cleared when configurations have been updated. (R/W/WTC)


## Register 9.72. PCR_SAR_CLK_DIV_REG (0x0148)

PCR_SAR2_CLK_DIV_NUM Configures the divisor for SAR ADC2 clock to generate ADC analog control signals. (R/W)
PCR_SAR1_CLK_DIV_NUM Configures the divisor for SAR ADC clock to generate ADC analog control signals. (R/W)
```