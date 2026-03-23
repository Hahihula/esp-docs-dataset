

```markdown
Register 8.66. PCR_AHB_FREQ_CONF_REG (0x011C)

PCR_AHB_LS_DIV_NUM Configures the divider of HP_ROOT_CLK to generate AHB_CLK.
O (default): HP_ROOT_CLK is divided by 1 to generate AHB_CLK
1: HP_ROOT_CLK is divided by 2 to generate AHB_CLK
3: HP_ROOT_CLK is divided by 4 to generate AHB_CLK
7: HP_ROOT_CLK is divided by 8 to generate AHB_CLK

This field is only available when a low-speed clock source such as XTAL/FOSC is selected, and should be used together with PCR_CPU_LS_DIV_NUM.
(R/W)

PCR_AHB_HS_DIV_NUM Configure the divider of HP_ROOT_CLK to generate AHB_CLK.
3 (default): HP_ROOT_CLK is divided by 4 to generate AHB_CLK
7: HP_ROOT_CLK is divided by 8 to generate AHB_CLK
15: HP_ROOT_CLK is divided by 16 to generate AHB_CLK

This field is only available when a high-speed clock source such as SP LL is selected, and should be used together with PCR_CPU_HS_DIV_NUM.
(R/W)
```