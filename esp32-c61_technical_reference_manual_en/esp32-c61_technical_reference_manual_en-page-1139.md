

```markdown
Register 30.30. SDIO_SLCOINT_RAW_REG (0x0004)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | SDIO_SLCO_RX_DSSCR_ERR_INT_RAW             | The raw interrupt status of SLCO_RX_DSSCR_ERR_INT. (R/WTC/SS)                |
| 29  | SDIO_SLCO_TX_DSCR_ERR_INT_RAW              | The raw interrupt status of SLCO_TX_DSCR_ERR_INT. (R/WTC/SS)                 |
| 28  | SDIO_SLCO_RX_EOF_INT_RAW                   | The raw interrupt status of SLCO_RX_EOF_INT. (R/WTC/SS)                      |
| 27  | SDIO_SLCO_TX_DONE_INT_RAW                  | The raw interrupt status of SLCO_TX_DONE_INT. (R/WTC/SS)                     |
| 26  | SDIO_SLCO_TX_SUC_EOF_INT_RAW               | The raw interrupt status of SLCO_TX_SUC_EOF_INT. (R/WTC/SS)                  |
| 25  | SDIO_SLCO_RX_OVF_INT_RAW                   | The raw interrupt status of SLCO_RX_OVF_INT. (R/WTC/SS)                      |
| 24  | SDIO_SLCO_TX_START_INT_RAW                 | The raw interrupt status of SLCO_TX_START_INT. (R/WTC/SS)                    |
| 23  | SDIO_SLCO_RX_UDF_INT_RAW                   | The raw interrupt status of SLCO_RX_UDF_INT. (R/WTC/SS)                      |
| 22  | SDIO_SLCO_TX_DONE_INT_RAW                  | The raw interrupt status of SLCO_TX_DONE_INT. (R/WTC/SS)                     |
| 21  | SDIO_SLCO_TX_SUC_EOF_INT_RAW               | The raw interrupt status of SLCO_TX_SUC_EOF_INT. (R/WTC/SS)                  |
| 20  | SDIO_SLCO_RX_OVF_INT_RAW                   | The raw interrupt status of SLCO_RX_OVF_INT. (R/WTC/SS)                      |
| 19  | SDIO_SLCO_TX_START_INT_RAW                 | The raw interrupt status of SLCO_TX_START_INT. (R/WTC/SS)                    |
| 18  | SDIO_SLCO_RX_UDF_INT_RAW                   | The raw interrupt status of SLCO_RX_UDF_INT. (R/WTC/SS)                      |
| 17  | SDIO_SLCO_RX_DSSCR_ERR_INT_RAW             | The raw interrupt status of SLCO_RX_DSSCR_ERR_INT. (R/WTC/SS)                |
| 16  | SDIO_SLCO_TX_DONE_INT_RAW                  | The raw interrupt status of SLCO_TX_DONE_INT. (R/WTC/SS)                     |
| 15  | SDIO_SLCO_TX_SUC_EOF_INT_RAW               | The raw interrupt status of SLCO_TX_SUC_EOF_INT. (R/WTC/SS)                  |
| 14  | SDIO_SLCO_RX_OVF_INT_RAW                   | The raw interrupt status of SLCO_RX_OVF_INT. (R/WTC/SS)                      |
| 13  | SDIO_SLCO_TX_START_INT_RAW                 | The raw interrupt status of SLCO_TX_START_INT. (R/WTC/SS)                    |
| 12  | SDIO_SLCO_RX_UDF_INT_RAW                   | The raw interrupt status of SLCO_RX_UDF_INT. (R/WTC/SS)                      |
| 11  | SDIO_SLCO_RX_DSSCR_ERR_INT_RAW             | The raw interrupt status of SLCO_RX_DSSCR_ERR_INT. (R/WTC/SS)                |
| 10  | SDIO_SLCO_TX_DONE_INT_RAW                  | The raw interrupt status of SLCO_TX_DONE_INT. (R/WTC/SS)                     |
| 9   | SDIO_SLCO_TX_SUC_EOF_INT_RAW               | The raw interrupt status of SLCO_TX_SUC_EOF_INT. (R/WTC/SS)                  |
| 8   | SDIO_SLCO_RX_OVF_INT_RAW                   | The raw interrupt status of SLCO_RX_OVF_INT. (R/WTC/SS)                      |
| 7   | SDIO_SLCO_TX_START_INT_RAW                 | The raw interrupt status of SLCO_TX_START_INT. (R/WTC/SS)                    |
| 6   | SDIO_SLCO_RX_UDF_INT_RAW                   | The raw interrupt status of SLCO_RX_UDF_INT. (R/WTC/SS)                      |
| 5   | SDIO_SLCO_RX_DSSCR_ERR_INT_RAW             | The raw interrupt status of SLCO_RX_DSSCR_ERR_INT. (R/WTC/SS)                |
| 4   | SDIO_SLCO_TX_DONE_INT_RAW                  | The raw interrupt status of SLCO_TX_DONE_INT. (R/WTC/SS)                     |
| 3   | SDIO_SLCO_TX_SUC_EOF_INT_RAW               | The raw interrupt status of SLCO_TX_SUC_EOF_INT. (R/WTC/SS)                  |
| 2   | SDIO_SLCO_RX_OVF_INT_RAW                   | The raw interrupt status of SLCO_RX_OVF_INT. (R/WTC/SS)                      |
| 1   | SDIO_SLCO_TX_START_INT_RAW                 | The raw interrupt status of SLCO_TX_START_INT. (R/WTC/SS)                    |
| 0   | Reset                                      | 0x0                                                                             |

SDIO_SLC_FRHOST_BITn_INT_RAW (n: 0-7) The raw interrupt status of SLC_FRHOST_BITn_INT (n: 0-7). (R/WTC/SS)

SDIO_SLCO_RX_START_INT_RAW The raw interrupt status of SLCO_RX_START_INT. (R/WTC/SS)

SDIO_SLCO_TX_START_INT_RAW The raw interrupt status of SLCO_TX_START_INT. (R/WTC/SS)

SDIO_SLCO_RX_UDF_INT_RAW The raw interrupt status of SLCO_RX_UDF_INT. (R/WTC/SS)

SDIO_SLCO_TX_OVF_INT_RAW The raw interrupt status of SLCO_TX_OVF_INT. (R/WTC/SS)

SDIO_SLCO_TX_DONE_INT_RAW The raw interrupt status of SLCO_TX_DONE_INT. (R/WTC/SS)

SDIO_SLCO_TX_SUC_EOF_INT_RAW The raw interrupt status of SLCO_TX_SUC_EOF_INT. (R/WTC/SS)

SDIO_SLCO_RX_DONE_INT_RAW The raw interrupt status of SLCO_RX_DONE_INT. (R/WTC/SS)

SDIO_SLCO_RX_EOF_INT_RAW The raw interrupt status of SLCO_RX_EOF_INT. (R/WTC/SS)

SDIO_SLCO_TX_DSCR_ERR_INT_RAW The raw interrupt status of SLCO_TX_DSCR_ERR_INT. (R/WTC/SS)

SDIO_SLCO_RX_DSCR_ERR_INT_RAW The raw interrupt status of SLCO_RX_DSCR_ERR_INT. (R/WTC/SS)
```