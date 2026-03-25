

```markdown
Register 7.24. PCR_I2S_TX_CLKM_CONF_REG (0x0064)

PCR_I2S_TX_CLKM_DIV_NUM Configures the integral I2S TX clock divider value.
(R/W)

PCR_I2S_TX_CLKM_SEL Configures the clock source of I2S TX.

O (default): XTAL_CLK
1: PLL_F120M_CLK
2: PLL_F160M_CLK
3: I2S_MCLK_in

(R/W)

PCR_I2S_TX_CLKM_EN Configures whether or not to enable I2S TX functional clock.
O: Not enable
1: Enable

(R/W)
```

```markdown
Register 7.25. PCR_I2S_TX_CLKM_DIV_CONF_REG (0x0068)

PCR_I2S_TX_CLKM_DIV_Z For b <= a/2, the value of I2S_TX_CLKM_DIV_Z is b. For b > a/2, the value of I2S_TX_CLKM_DIV_Z is (a-b). (R/W)

PCR_I2S_TX_CLKM_DIV_Y For b <= a/2, the value of I2S_TX_CLKM_DIV_Y is (a%b) . For b > a/2, the value of I2S_TX_CLKM_DIV_Y is (a%(a-b)). (R/W)

PCR_I2S_TX_CLKM_DIV_X For b <= a/2, the value of I2S_TX_CLKM_DIV_X is (a/b) - 1. For b > a/2, the value of I2S_TX_CLKM_DIV_X is (a/(a-b)) - 1. (R/W)

PCR_I2S_TX_CLKM_DIV_YN1 For b <= a/2, the value of I2S_TX_CLKM_DIV_YN1 is 0 . For b > a/2, the value of I2S_TX_CLKM_DIV_YN1 is 1. (R/W)
```