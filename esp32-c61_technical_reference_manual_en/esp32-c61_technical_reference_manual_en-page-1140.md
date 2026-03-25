

```markdown
Register 30.31. SDIO_SLCOINT_ST_REG (0x0008)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | SDIO_SLCO_RX_DSRR_ERR_INT_ST                                                 |
| 29  | SDIO_SLCO_TX_DSCR_ERR_INT_ST                                                |
| 28  | (reserved)                                                                  |
| 27  | SDIO_SLCO_RX_EOF_INT_ST                                                     |
| 26  | SDIO_SLCO_TX_DONE_INT_ST                                                    |
| 25  | SDIO_SLCO_RX_DONE_INT_ST                                                    |
| 24  | SDIO_SLCO_TX_OVF_INT_ST                                                     |
| 23  | SDIO_SLCO_RX_UDF_INT_ST                                                     |
| 22  | SDIO_SLCO_TX_START_INT_ST                                                   |
| 21  | SDIO_SLCO_RX_START_INT_ST                                                   |
| 20  | (reserved)                                                                  |
| 19  | SDIO_SLC0_FRHOST_BITn_INT_ST (n: 0-7)                                      |
| 18  | SDIO_SLCO_TX_SUC_EOF_INT_ST                                                 |
| 17  | SDIO_SLCO_RX_DONE_INT_ST                                                    |
| 16  | SDIO_SLCO_TX_DONE_INT_ST                                                    |
| 15  | SDIO_SLCO_RX_EOF_INT_ST                                                     |
| 14  | SDIO_SLCO_TX_OVF_INT_ST                                                     |
| 13  | SDIO_SLCO_RX_UDF_INT_ST                                                     |
| 12  | SDIO_SLCO_TX_START_INT_ST                                                   |
| 11  | SDIO_SLCO_RX_START_INT_ST                                                   |
| 10  | (reserved)                                                                  |
| 9   | SDIO_SLC0_FRHOST_BITn_INT_ST (n: 0-7)                                      |
| 8   | SDIO_SLCO_TX_DSCR_ERR_INT_ST                                                |
| 7   | SDIO_SLCO_RX_DSCR_ERR_INT_ST                                                |
| 6   | (reserved)                                                                  |
| 5   | SDIO_SLC0_FRHOST_BITn_INT_ST (n: 0-7)                                      |
| 4   | SDIO_SLCO_TX_DONE_INT_ST                                                    |
| 3   | SDIO_SLCO_RX_DONE_INT_ST                                                    |
| 2   | SDIO_SLCO_RX_EOF_INT_ST                                                     |
| 1   | SDIO_SLCO_TX_OVF_INT_ST                                                     |
| 0   | Reset                                                                       |

SDIO_SLC0_FRHOST_BITn_INT_ST (n: 0-7) The masked interrupt status of SLC0_FRHOST_BITn_INT (n: 0-7). (RO)

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