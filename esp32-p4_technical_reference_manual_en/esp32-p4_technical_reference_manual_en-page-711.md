

```markdown
Register 10.43. HP_SYS_CLKRST_PERI_CLK_CTRL25_REG (0x00A8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | 1  | O  | O  | O  | O  | O  | O  | O  | O  | O  | O  | O  |
|     |    | HP_SYS_CLKRST_SP_CLK_EN | HP_SYS_CLKRST_JSP_CLK_SRC_SEL | HP_SYS_CLKRST_CRYPTO_KM_CLK_EN | HP_SYS_CLKRST_CRYPTO_EODSA_CLK_EN | HP_SYS_CLKRST_CRYPTO_SHA_CLK_EN | HP_SYS_CLKRST_CRYPTO_SEC_CLK_EN | HP_SYS_CLKRST_CRYPTO_RSA_CLK_EN | HP_SYS_CLKRST_CRYPTO_HMAC_CLK_EN | HP_SYS_CLKRST_CRYPTO_ECC_CLK_EN | (reserved) |
|     |    |                          |                               |                                |                                 |                                 |                                 |                                 |                                 |                                 |            |

HP_SYS_CLKRST_CRYPTO_CLK_SRC_SEL Configures the clock source for CRYPTO_CLK.
O: XTAL_CLK
1: RC_FAST_CLK
2: PLL_F240M_CLK
3: PLL_F160M_CLK
(R/W)

HP_SYS_CLKRST_CRYPTO_AES_CLK_EN Configures whether to enable AES_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_CRYPTO_DSA_CLK_EN Configures whether to enable the RSA_DS clock.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_CRYPTO_ECC_CLK_EN Configures whether to enable ECC_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_CRYPTO_HMAC_CLK_EN Configures whether to enable HMAC_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_CRYPTO_RSA_CLK_EN Configures whether to enable RSA_CLK.
O: Disable
1: Enable
(R/W)

Continued on the next page...
```