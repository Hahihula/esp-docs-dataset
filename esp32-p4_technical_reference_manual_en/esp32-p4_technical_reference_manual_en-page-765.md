

```markdown
Register 10.73. LPPERI_CORE_CLK_SEL_REG (0x0004)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | ... | Reset |
|-----|----|----|----|----|----|----|----|----|----|------|-------|
|     |    | LPPERI_LP_UART_CLK_SEL | LPPERI_LP_I2C_CLK_SEL | LPPERI_LP_I2S_RX_CLK_SEL | (reserved) | ... | 0x0 | 0x0 | 0x0 |       |

LPPERI_LP_I2S_RX_CLK_SEL   Configures LP I2S RX clock source.
    0: LP_FAST_CLK
    1: XTAL_D2_CLK
    2: PLL_LP_CLK
    3: Invalid
        (R/W)

LPPERI_LP_I2C_CLK_SEL      Configures LP I2C clock source.
    0: LP_FAST_CLK
    1: XTAL_D2_CLK
    2: PLL_LP_CLK
    3: Invalid
        (R/W)

LPPERI_LP_UART_CLK_SEL     Configures LP UART clock source.
    0: RC_FAST_CLK
    1: XTAL_D2_CLK
    2: PLL_LP_CLK
    3: Invalid
        (R/W)
```