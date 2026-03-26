

```markdown
Register 10.67. LP_CLKRST_HP_CLK_CTRL_REG (0x0040)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 0   |
|     |    |    | (reserved) | LP_CLKRST_HP_MPLL_500M_CLK_EN | LP_CLKRST_HP_MPLL_480M_CLK_EN | LP_CLKRST_HP_MPLL_400M_CLK_EN | LP_CLKRST_HP_MPLL_20M_CLK_EN | LP_CLKRST_HP_XTAL_CLK_EN | LP_CLKRST_HP_PAD_EMAC_TX_CLK_EN | LP_CLKRST_HP_PAD_EMAC_RX_CLK_EN | LP_CLKRST_HP_PAD_SLP_CLK_EN | LP_CLKRST_HP_PAD_UART4_SLP_CLK_EN | LP_CLKRST_HP_PAD_UART3_SLP_CLK_EN | LP_CLKRST_HP_PAD_PARLIO_TX_CLK_EN | LP_CLKRST_HP_PAD_PARLIO_RX_CLK_EN | LP_CLKRST_HP_SRC_SEL |
```

LP_CLKRST_HP_ROOT_CLK_SRC_SEL Configures the clock source of ROOT_CLK.

O: XTAL_CLK

1: CPLL_CLK (360 MHz)

2: RC_FAST_CLK

3: Invalid

(R/W)

LP_CLKRST_HP_ROOT_CLK_EN Configures whether to enable ROOT_CLK.

O: Disable

1: Enable

(R/W)

LP_CLKRST_HP_PAD_PARLIO_TX_CLK_EN Configures whether to enable PAD_PARLIO_TX_CLK from IO pin.

O: Disable

1: Enable

(R/W)

LP_CLKRST_HP_PAD_PARLIO_RX_CLK_EN Configures whether to enable PAD_PARLIO_RX_CLK from IO pin.

O: Disable

1: Enable

(R/W)

LP_CLKRST_HP_PAD_UART4_SLP_CLK_EN Configures whether to enable PAD_UART4_SLP_CLK from IO pin.

O: Disable

1: Enable

(R/W)

LP_CLKRST_HP_PAD_UART3_SLP_CLK_EN Configures whether to enable PAD_UART3_SLP_CLK from IO pin.

O: Disable

1: Enable

(R/W)

Continued on the next page...
```