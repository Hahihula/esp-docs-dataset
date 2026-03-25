
```markdown
Register 39.30. SDIO_SLCOINT_RAW_REG (0x0004)

| Bit | Field Name                             | Description                                                                 |
|-----|-----------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                             |                                                                             |
| 30  | SDIO_SLCO_RX_DSSCR_ERR_INT_RAW         | The raw interrupt status of SLCO_RX_DSSCR_ERR_INT. (R/WTC/SS)               |
| 29  | SDIO_SLCO_TX_ERR_INT_RAW               | The raw interrupt status of SLCO_TX_ERR_INT. (R/WTC/SS)                     |
| 28  | SDIO_SLCO_RX_DONE_INT_RAW              | The raw interrupt status of SLCO_RX_DONE_INT. (R/WTC/SS)                    |
| 27  | SDIO_SLCO_TX_SUC_EOF_INT_RAW           | The raw interrupt status of SLCO_TX_SUC_EOF_INT. (R/WTC/SS)                 |
| 26  | SDIO_SLCO_RX_EOF_INT_RAW               | The raw interrupt status of SLCO_RX_EOF_INT. (R/WTC/SS)                     |
| 25  | SDIO_SLCO_TX_DONE_INT_RAW              | The raw interrupt status of SLCO_TX_DONE_INT. (R/WTC/SS)                    |
| 24  | SDIO_SLCO_TX_OVF_INT_RAW               | The raw interrupt status of SLCO_TX_OVF_INT. (R/WTC/SS)                     |
| 23  | SDIO_SLCO_RX_UDF_INT_RAW               | The raw interrupt status of SLCO_RX_UDF_INT. (R/WTC/SS)                     |
| 22  | SDIO_SLCO_TX_START_INT_RAW             | The raw interrupt status of SLCO_TX_START_INT. (R/WTC/SS)                   |
| 21  | SDIO_SLCO_RX_START_INT_RAW             | The raw interrupt status of SLCO_RX_START_INT. (R/WTC/SS)                   |
| 20  | SDIO_SLC_FRHOST_BITn_INT_RAW           | The raw interrupt status of SLC_FRHOST_BITn_INT (n: 0-7). (R/WTC/SS)        |
| 19  | (reserved)                             |                                                                             |
| 18  | (reserved)                             |                                                                             |
| 17  | (reserved)                             |                                                                             |
| 16  | (reserved)                             |                                                                             |
| 15  | (reserved)                             |                                                                             |
| 14  | (reserved)                             |                                                                             |
| 13  | (reserved)                             |                                                                             |
| 12  | (reserved)                             |                                                                             |
| 11  | (reserved)                             |                                                                             |
| 10  | (reserved)                             |                                                                             |
| 9   | (reserved)                             |                                                                             |
| 8   | (reserved)                             |                                                                             |
| 7   | (reserved)                             |                                                                             |
| 6   | (reserved)                             |                                                                             |
| 5   | (reserved)                             |                                                                             |
| 4   | (reserved)                             |                                                                             |
| 3   | (reserved)                             |                                                                             |
| 2   | (reserved)                             |                                                                             |
| 1   | (reserved)                             |                                                                             |
| 0   | Reset                                   | All bits are reset to 0.                                                   |

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