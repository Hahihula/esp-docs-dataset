

```markdown
Register 8.65. PCR_CPU_FREQ_CONF_REG (0x0118)

PCR_CPU_LS_DIV_NUM Configures the divider of HP_ROOT_CLK to generate CPU_CLK.
- 0 (default): The HP_ROOT_CLK is divided by 1 to generate CPU_CLK
- 1: The HP_ROOT_CLK is divided by 2 to generate CPU_CLK
- 3: The HP_ROOT_CLK is divided by 4 to generate CPU_CLK

This field is only available when a low-speed clock source such as XTAL/FOSC is selected, and should be used together with PCR_AHB_LS_DIV_NUM.
(R/W)

PCR_CPU_HS_DIV_NUM Configures the divider of HP_ROOT_CLK to generate CPU_CLK.
- 0 (default): The HP_ROOT_CLK is divided by 1 to generate CPU_CLK
- 1: The HP_ROOT_CLK is divided by 2 to generate CPU_CLK
- 3: The HP_ROOT_CLK is divided by 4 to generate CPU_CLK

This field is only available when a high-speed clock source such as SP LL is selected, and should be used together with PCR_AHB_HS_DIV_NUM.
(R/W)

PCR_CPU_HS_120M_FORCE Configures whether or not to force CPU_CLK at 120 MHz when PCR_CPU_HS_DIV_NUM is 0.
- 0: Not force CPU_CLK at 120 MHz
- 1: Force CPU_CLK at 120 MHz

This bit is only available when PCR_CPU_HS_DIV_NUM is 0 and CPU_CLK is derived from SP LL.
(R/W)
```