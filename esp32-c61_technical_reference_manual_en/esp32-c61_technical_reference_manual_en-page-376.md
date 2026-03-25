

```markdown
Register 7.57. PCR_BUS_CLK_UPDATE_REG (0x0120)

PCR_BUS_CLOCK_UPDATE Configures whether or not to update configurations for CPU_CLK division, AHB_CLK division and HP_ROOT_CLK clock source selection.
- 0: Not update configurations
- 1: Update configurations

This bit is automatically cleared when configurations have been updated.

(R/W/WTC)
```

```markdown
Register 7.58. PCR_SAR_CLK_DIV_REG (0x0124)

PCR_SAR2_CLK_DIV_NUM Configures the divisor for SAR ADC2 clock to generate ADC analog control signals.
(R/W)

PCR_SAR1_CLK_DIV_NUM Configures the divisor for SAR ADC1 clock to generate ADC analog control signals.
(R/W)
```