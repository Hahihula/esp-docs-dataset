

```markdown
Register 7.52. PCR_AHB_FREQ_CONF_REG (0x00F4)

PCR_AHB_DIV_NUM Configures the divisor of HP_ROOT_CLK to generate AHB_CLK.
This field should be used together with PCR_CPU_DIV_NUM.
(R/W)
```

```markdown
Register 7.53. PCR_APB_FREQ_CONF_REG (0x00F8)

PCR_APB_DECREASE_DIV_NUM Configures the divisor AHB_CLK to generate APB_CLK during the first division.
(R/W)

PCR_APB_DIV_NUM Configures the divisor of AHB_CLK to generate APB_CLK during the second division.
(R/W)
```