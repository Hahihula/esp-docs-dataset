

```markdown
Chapter 8 Reset and Clock

Register 8.67. PCR_APB_FREQ_CONF_REG (0x0120)

PCR_APB_DECREASE_DIV_NUM Configures the divider of APB_CLK to generate APB_DECREASE_CLK.
O: APB_CLK is divided by 1 to generate APB_DECREASE_CLK
1: APB_CLK is divided by 2 to generate APB_DECREASE_CLK
3 (default): APB_CLK is divided by 4 to generate APB_DECREASE_CLK

If the value of this field is greater than PCR_APB_DIV_NUM, APB_CLK will be automatically down to APB_DECREASE_CLK only when no access is on APB bus, and will recover to the previous frequency when a new access appears on APB bus. Note that enabling this function will reduce performance. Users can set this field as zero to disable the auto-decrease-APB-freq function. By default, this function is disabled.
(R/W)

PCR_APB_DIV_NUM Configures the divider of AHB_CLK to generate APB_CLK.
O (default): AHB_CLK is divided by 1 to generate APB_CLK
1: AHB_CLK is divided by 2 to generate APB_CLK
3: AHB_CLK is divided by 4 to generate APB_CLK
(R/W)
```