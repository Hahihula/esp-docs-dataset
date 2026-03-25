

```markdown
Register 39.31. SDIO_SLCOINT_ST_REG (0x0008)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    | (reserved) | SDIO_SLCO_RX_DSCR_ERR_INT_ST | SDIO_SLCO_TX_DSCR_ERR_INT_ST | (reserved) | SDIO_SLCO_RX_EOF_INT_ST | SDIO_SLCO_TX_DONE_INT_ST | SDIO_SLCO_RX_DONE_INT_ST | SDIO_SLCO_TX_SUC_EOF_INT_ST | SDIO_SLCO_TX_OVF_INT_ST | SDIO_SLCO_RX_UDF_INT_ST | SDIO_SLCO_TX_START_INT_ST | SDIO_SLCO_RX_START_INT_ST |    |
| Value (Reset) | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
```

SDIO_SLC_FRHOST_BITn_INT_ST (n: 0-7) The masked interrupt status of SLC_FRHOST_BITn_INT (n: 0-7). (RO)

SDIO_SLCO_RX_START_INT_ST The masked interrupt status of SLCO_RX_START_INT. (RO)

SDIO_SLCO_TX_START_INT_ST The masked interrupt status bit of SLCO_TX_START_INT. (RO)

SDIO_SLCO_RX_UDF_INT_ST The masked interrupt status of SLCO_RX_UDF_INT. (RO)

SDIO_SLCO_TX_OVF_INT_ST The masked interrupt status of SLCO_TX_OVF_INT. (RO)

SDIO_SLCO_TX_DONE_INT_ST The masked interrupt status of SLCO_TX_DONE_INT. (RO)

SDIO_SLCO_TX_SUC_EOF_INT_ST The masked interrupt status of SLCO_TX_SUC_EOF_INT. (RO)

SDIO_SLCO_RX_DONE_INT_ST The masked interrupt status of SLCO_RX_DONE_INT. (RO)

SDIO_SLCO_RX_EOF_INT_ST The masked interrupt status bit of SLCO_RX_EOF_INT. (RO)

SDIO_SLCO_TX_DSCR_ERR_INT_ST The masked interrupt status of SLCO_TX_DSCR_ERR_INT. (RO)

SDIO_SLCO_RX_DSCR_ERR_INT_ST The masked interrupt status of SLCO_RX_DSCR_ERR_INT. (RO)
```