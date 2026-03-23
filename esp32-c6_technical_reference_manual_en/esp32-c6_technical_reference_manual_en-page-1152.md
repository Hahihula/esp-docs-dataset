
```markdown
Register 34.38. SDIO_SLC1INT_ENA1_REG (0x0150)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    | (reserved) | SDIO_SLC1_RX_DSCR_ERR_INT_ENA1 | SDIO_SLC1_TX_DONE_INT_ENA1 | SDIO_SLC1_RX_OVF_INT_ENA1 | SDIO_SLC1_TX_SUC_EOF_INT_ENA1 | SDIO_SLC1_RX_DONE_INT_ENA1 | SDIO_SLC1_TX_EOF_INT_ENA1 | (reserved) | SDIO_SLC1_RX_ERR_INT_ENA1 | SDIO_SLC1_TX_ERR_INT_ENA1 | SDIO_SLC1_RX_DSCR_ERR_INT_ENA1 | (reserved) | SDIO_SLC1_TX_OVF_INT_ENA1 | SDIO_SLC1_RX_UDF_INT_ENA1 | SDIO_SLC1_TX_START_INT_ENA1 | SDIO_SLC1_RX_START_INT_ENA1 |
| Value | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

SDIO_SLC_FRHOST_BITn_INT_ENA1 (n: 8-15) Write 1 to enable interrupt SLC_FRHOST_BITn_INT
(n: 8-15). (R/W)

SDIO_SLC1_RX_START_INT_ENA1 Write 1 to enable interrupt SLC1_RX_START_INT. (R/W)

SDIO_SLC1_TX_START_INT_ENA1 Write 1 to enable interrupt SLC1_TX_START_INT. (R/W)

SDIO_SLC1_RX_UDF_INT_ENA1 Write 1 to enable interrupt SLC1_RX_UDF_INT. (R/W)

SDIO_SLC1_TX_OVF_INT_ENA1 Write 1 to enable interrupt SLC1_TX_OVF_INT. (R/W)

SDIO_SLC1_TX_DONE_INT_ENA1 Write 1 to enable interrupt SLC1_TX_DONE_INT. (R/W)

SDIO_SLC1_TX_SUC_EOF_INT_ENA1 Write 1 to enable interrupt SLC1_TX_SUC_EOF_INT. (R/W)

SDIO_SLC1_RX_DONE_INT_ENA1 Write 1 to enable interrupt SLC1_RX_DONE_INT. (R/W)

SDIO_SLC1_RX_EOF_INT_ENA1 Write 1 to enable interrupt SLC1_RX_EOF_INT. (R/W)

SDIO_SLC1_TX_DSCR_ERR_INT_ENA1 Write 1 to enable interrupt SLC1_TX_DSCR_ERR_INT. (R/W)

SDIO_SLC1_RX_DSCR_ERR_INT_ENA1 Write 1 to enable interrupt SLC1_RX_DSCR_ERR_INT. (R/W)


Register 34.39. SDIO_SLCO_LENGTH_REG (0x00F8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    | (reserved) | SDIO_SLCO_EN | Ox0 | Ox0 | Reset |
```