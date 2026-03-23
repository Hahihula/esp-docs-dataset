

```markdown
Register 34.31. SDIO_SLCOINT_ST_REG (0x0008)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | SDIO_SLCO_RX_DSCR_ERR_INT_ST                                                |
| 29  | SDIO_SLCO_TX_DSCR_ERR_INT_ST                                                |
| 28  | (reserved)                                                                  |
| 27  | SDIO_SLCO_RX_EOF_INT_ST                                                     |
| 26  | SDIO_SLCO_TX_DONE_INT_ST                                                    |
| 25  | SDIO_SLCO_TX_OVF_INT_ST                                                     |
| 24  | SDIO_SLCO_RX_UDF_INT_ST                                                     |
| 23  | SDIO_SLCO_TX_START_INT_ST                                                   |
| 22  | SDIO_SLCO_RX_START_INT_ST                                                   |
| 21  | (reserved)                                                                  |
| 20  | OxD0                                                                        |
| 19  | OxD0                                                                        |
| 18  | OxD0                                                                        |
| 17  | OxD0                                                                        |
| 16  | OxD0                                                                        |
| 15  | OxD0                                                                        |
| 14  | OxD0                                                                        |
| 13  | OxD0                                                                        |
| 12  | OxD0                                                                        |
| 11  | OxD0                                                                        |
| 10  | OxD0                                                                        |
| 9   | OxD0                                                                        |
| 8   | OxD0                                                                        |
| 7   | OxD0                                                                        |
| 6   | OxD0                                                                        |
| 5   | OxD0                                                                        |
| 4   | OxD0                                                                        |
| 3   | OxD0                                                                        |
| 2   | OxD0                                                                        |
| 1   | OxD0                                                                        |
| 0   | Reset                                                                       |

SDIO_SLC_FRHOST_BITn_INT_ST (n: 0-7) The masked interrupt status of SLC_FRHOST_BITn_INT
(n: 0-7). (RO)

SDIO_SLCO_RX_START_INT_ST The masked interrupt status of SLCO_RX_START_INT. (RO)

SDIO_SLCO_TX_START_INT_ST The masked interrupt status bit of SLCO_TX_START_INT. (RO)

SDIO_SLCO_RX_UDF_INT_ST The masked interrupt status of SLCO_RX_UDF_INT. (RO)

SDIO_SLCO_TX_OVF_INT_ST The masked interrupt status of SLCO_TX_OVF_INT. (RO)

SDIO_SLCO_TX_DONE_INT_ST The masked interrupt status of SLCO_TX_DONE_INT. (RO)

SDIO_SLCO_TX_SUC_EOF_INT_ST The masked interrupt status of SLCO_TX_SUC_EOF_INT. (RO)

SDIO_SLCO_RX_DONE_INT_ST The masked interrupt status of SLCO_RX_DONE_INT. (RO)

SDIO_SLCO_RX_EOF_INT_ST The masked interrupt status bit of SLCO_RX_EOF_INT. (RO)

SDIO_SLCO_TX_DSCR_ERR_INT_ST The masked interrupt status of SLCO_TX_DSCR_ERR_INT.
(RO)

SDIO_SLCO_RX_DSCR_ERR_INT_ST The masked interrupt status of SLCO_RX_DSCR_ERR_INT.
(RO)
```