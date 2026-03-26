

```markdown
Register 10.14. HP_SYS_CLKRST_PERI_CLK_CTRL01_REG (0x0034)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | HP_SYS_CLKRST_SDIO_LS_CLK_EN               |                                                                             |
| 29  | HP_SYS_CLKRST_SDIO_LS_CLK_SRC_SEL          |                                                                             |
| 28  | HP_SYS_CLKRST_SDIO_HS_MODE                 |                                                                             |
| 27  | (reserved)                                 |                                                                             |
| 26  | HP_SYS_CLKRST_EMAC_PTP_REF_CLK_EN          | Configures whether to enable EMAC_PTP_REF_CLK.                              |
| 25  | HP_SYS_CLKRST_EMAC_TX_CLK_SRC_SEL          | Configures the clock source for EMAC_TX_CLK.                                |
| 24  | HP_SYS_CLKRST_EMAC_TX_CLK_EN               | Configures whether to enable EMAC_TX_CLK.                                   |
| 23  | HP_SYS_CLKRST_EMAC_TX_CLK_DIV_NUM          | Configures the clock divisor for EMAC_TX_CLK. (R/W)                          |
| 22  | HP_SYS_CLKRST_EMAC_PTP_REF_CLK_SRC_SEL     | Configures the clock source for EMAC_PTP_REF_CLK.                           |
| 21  | O: XTAL_CLK                                |                                                                                 |
| 20  | 1: PLL_F80M_CLK                            |                                                                                 |
| 19  | (reserved)                                 |                                                                             |
| 18  | HP_SYS_CLKRST_EMAC_RX_CLK_DIV_NUM          | Configures the clock divisor for EMAC_RX_CLK. (R/W)                          |
| 17  | O: Disable                                 |                                                                                 |
| 16  | 1: Enable                                  |                                                                                 |
| 15  | (reserved)                                 |                                                                             |
| 14  | HP_SYS_CLKRST_EMAC_TX_CLK_SRC_SEL          | Configures the clock source for EMAC_TX_CLK.                                |
| 13  | O: PAD_EMAC_TXRX_CLK                       |                                                                                 |
| 12  | 1: PAD_EMAC_TX_CLK                         |                                                                                 |
| 11  | (reserved)                                 |                                                                             |
| 10  | HP_SYS_CLKRST_EMAC_TX_CLK_EN               | Configures whether to enable EMAC_TX_CLK.                                   |
| 9   | O: Disable                                 |                                                                                 |
| 8   | 1: Enable                                  |                                                                                 |
| 7   | (reserved)                                 |                                                                             |
| 6   | HP_SYS_CLKRST_EMAC_RX_CLK_DIV_NUM          | Configures the clock divisor for EMAC_RX_CLK. (R/W)                          |
| 5   | O: Disable                                 |                                                                                 |
| 4   | 1: Enable                                  |                                                                                 |
| 3   | (reserved)                                 |                                                                             |
| 2   | HP_SYS_CLKRST_SDIO_LS_CLK_EN               |                                                                             |
| 1   | HP_SYS_CLKRST_SDIO_LS_CLK_SRC_SEL          |                                                                             |
| 0   | Reset                                      |                                                                             |

HP_SYS_CLKRST_EMAC_RX_CLK_DIV_NUM Configures the clock divisor for EMAC_RX_CLK. (R/W)

HP_SYS_CLKRST_EMAC_TX_CLK_SRC_SEL Configures the clock source for EMAC_TX_CLK.
O: PAD_EMAC_TXRX_CLK
1: PAD_EMAC_TX_CLK
(R/W)

HP_SYS_CLKRST_EMAC_TX_CLK_EN Configures whether to enable EMAC_TX_CLK.
O: Disable
1: Enable
(R/W)

HP_SYS_CLKRST_EMAC_TX_CLK_DIV_NUM Configures the clock divisor for EMAC_TX_CLK. (R/W)

HP_SYS_CLKRST_EMAC_PTP_REF_CLK_SRC_SEL Configures the clock source for EMAC_PTP_REF_CLK.
O: XTAL_CLK
1: PLL_F80M_CLK
(R/W)

HP_SYS_CLKRST_EMAC_PTP_REF_CLK_EN Configures whether to enable EMAC_PTP_REF_CLK.
O: Disable
1: Enable
(R/W)

Continued on the next page...
```