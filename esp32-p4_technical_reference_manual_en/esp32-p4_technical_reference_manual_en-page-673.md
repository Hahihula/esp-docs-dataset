

```markdown
Register 10.11. HP_SYS_CLKRST_REF_CLK_CTRL1_REG (0x0028)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 24 | 23 | 22 | 21 | 20 | 16 | 15 | 8 | 7 | 3 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|
|     |    | (reserved) HP_SYS_CLKRST_REF_240M_CLK_EN | (reserved) HP_SYS_CLKRST_REF_25M_CLK_EN | HP_SYS_CLKRST_REF_50M_CLK_EN | (reserved) | HP_SYS_CLKRST_REF_20M_CLK_DIV_NUM | HP_SYS_CLKRST_REF_80M_CLK_DIV_NUM | HP_SYS_CLKRST_REF_120M_CLK_DIV_NUM | Reset |
| Value | 0 | 1 | 0 | 1 | 0 | 0 | 23 |    |    |    |    | 5 |    |    |    |    |    |

HP_SYS_CLKRST_REF_120M_CLK_DIV_NUM Configures the divisor of PLL_F120M_CLK. (R/W)

HP_SYS_CLKRST_REF_80M_CLK_DIV_NUM Configures the divisor of PLL_F80M_CLK. (R/W)

HP_SYS_CLKRST_REF_20M_CLK_DIV_NUM Configures the divisor of PLL_F20M_CLK. (R/W)

HP_SYS_CLKRST_REF_50M_CLK_EN Configures whether to enable PLL_F50M_CLK.
    0: Disable
    1: Enable
    (R/W)

HP_SYS_CLKRST_REF_25M_CLK_EN Configures whether to enable PLL_F25M_CLK.
    0: Disable
    1: Enable
    (R/W)

HP_SYS_CLKRST_REF_240M_CLK_EN Configures whether to enable PLL_F240M_CLK.
    0: Disable
    1: Enable
    (R/W)
```