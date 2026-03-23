

```markdown
Register 34.18. SDIO_SLCCONF1_REG (0x0070)

| 31 | reserved | SDIO_SLC1_RX_STITCH_EN | SDIO_SLC1_TX_STITCH_EN | SDIO_HOST_INT_LEVEL_SEL | reserved | SDIO_SLCO_RX_STITCH_EN | SDIO_SLCO_TX_STITCH_EN | SDIO_SLCO_LEN_AUTO_CLR | SDIO_SLCO_CMD_HOLD_EN |
|-----|----------|------------------------|------------------------|-------------------------|----------|------------------------|------------------------|------------------------|-----------------------|
|     |          |                        |                        |                         |          |                        |                        |                        |                       |
| 0x0 | 22       | 1                      | 1                      | 0                       | Ox0      | 7                      | 6                      | 5                      | 4                     |
|     |          |                        |                        |                         |          | 1                      | 1                      | 1                      | 1                     |
| Reset|          |                        |                        |                         |          |                        |                        |                        |                       |

SDIO_SDIO_CMD_HOLD_EN Please initialize to 0, and do not modify it. (R/W)
SDIO_SLCO_LEN_AUTO_CLR Please initialize to 0, and do not modify it. (R/W)
SDIO_SLCO_TX_STITCH_EN Please initialize to 0, and do not modify it. (R/W)
SDIO_SLCO_RX_STITCH_EN Please initialize to 0, and do not modify it. (R/W)
SDIO_HOST_INT_LEVEL_SEL Configures the polarity of interrupt to host.
    0: Low active
    1: High active
(R/W)
SDIO_SLC1_TX_STITCH_EN Please initialize to 0, and do not modify it. (R/W)
SDIO_SLC1_RX_STITCH_EN Please initialize to 0, and do not modify it. (R/W)

Register 34.19. SDIO_SLC_RX_DSCR_CONF_REG (0x00A8)

| 31 | reserved |
|-----|----------|
|     |          |

SDIO_SLCO_TOKEN_NO_REPLACE Please initialize to 1, and do not modify it. (R/W)
```