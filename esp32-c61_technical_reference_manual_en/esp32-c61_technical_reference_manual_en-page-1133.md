

```markdown
Register 30.18. SDIO_SLCCONF1_REG (0x0070)

| 31 | (reserved) | 22 | 21 | 20 | 19 | 18 | (reserved) | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|------------|-----|----|----|----|----|------------|---|---|---|---|---|---|---|---|
|     |            |     |    |    |    |    |            |   |   |   |   |   |   |   |   |
| 0x0 |           | 1  | 1 | 0 |     | Ox0 |           | 1 | 1 | 1 | 1 | Ox0 | Reset |

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

Register 30.19. SDIO_SLC_RX_DSCR_CONF_REG (0x00A8)

| 31 | (reserved) | 0 |
|-----|------------|---|
|     |            |   |
| Ox101b80d |       | 0 Reset |

SDIO_SLCO_TOKEN_NO_REPLACE Please initialize to 1, and do not modify it. (R/W)
```