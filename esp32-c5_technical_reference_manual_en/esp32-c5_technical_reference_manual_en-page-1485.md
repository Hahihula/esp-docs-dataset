

```markdown
Register 39.35. SDIO_SLC1INT_CLR_REG (0x0020)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|:----|
| 0x0 | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O | O |

SDIO_SLC_FRHOST_BITn_INT_CLR (n: 8-15) Write 1 to clear interrupt SLC_FRHOST_BITn_INT (n: 8-15). (WT)

SDIO_SLC1_RX_START_INT_CLR Write 1 to clear interrupt SLC1_RX_START_INT. (WT)

SDIO_SLC1_TX_START_INT_CLR Write 1 to clear interrupt SLC1_TX_START_INT. (WT)

SDIO_SLC1_RX_UDF_INT_CLR Write 1 to clear interrupt SLC1_RX_UDF_INT. (WT)

SDIO_SLC1_TX_OVF_INT_CLR Write 1 to clear interrupt SLC1_TX_OVF_INT. (WT)

SDIO_SLC1_TX_DONE_INT_CLR Write 1 to clear interrupt SLC1_TX_DONE_INT. (WT)

SDIO_SLC1_TX_SUC_EOF_INT_CLR Write 1 to clear interrupt SLC1_TX_SUC_EOF_INT. (WT)

SDIO_SLC1_RX_DONE_INT_CLR Write 1 to clear interrupt SLC1_RX_DONE_INT. (WT)

SDIO_SLC1_RX_EOF_INT_CLR Write 1 to clear interrupt SLC1_RX_EOF_INT. (WT)

SDIO_SLC1_TX_DSCR_ERR_INT_CLR Write 1 to clear interrupt SLC1_TX_DSCR_ERR_INT. (WT)

SDIO_SLC1_RX_DSCR_ERR_INT_CLR Write 1 to clear interrupt SLC1_RX_DSCR_ERR_INT. (WT)


Register 39.36. SDIO_SLCINTVEC_TOHOST_REG (0x005C)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----:|:----|:----|:----|:----|:----|:----|
| 0x0 | 0x0 |     | 0x0 |     | 0x0 | Reset |

SDIO_SLC0_TOHOST_INTVEC The interrupt set bit of SLCHOST_SLC0_TOHOST_BITn_INT (n: 0-7). These bits will be cleared automatically. (WT)

SDIO_SLC1_TOHOST_INTVEC The interrupt set bit of SLCHOST_SLC1_TOHOST_BITn_INT (n: 0-7). These bits will be cleared automatically. (WT)
```