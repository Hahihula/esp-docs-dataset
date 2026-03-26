
```markdown
Register 43.97. LP_SPI_DMA_INT_RAW_REG (0x003C)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | LP_SPI_APP2_INT_RAW                        | The raw interrupt status of SPI_APP2_INT interrupt.                         |
| 29  | LP_SPI_MST_TX_AFIFO_REMPTY_ERR_INT_RAW     | The raw interrupt status of SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt.       |
| 28  | LP_SPI_MST_RX_AFIFO_WFULL_ERR_INT_RAW      | The raw interrupt status of SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt.        |
| 27  | LP_SPI_SLV_CMD_ERR_INT_RAW                 | The raw interrupt status of SPI_SLV_CMD_ERR_INT interrupt.                  |
| 26  | LP_SPI_SLV_BUF_ADDR_ERR_INT_RAW            | The raw interrupt status of SPI_SLV_BUF_ADDR_ERR_INT interrupt.             |
| 25  | LP_SPI_WAKEUP_INT_RAW                      | The raw interrupt status of LP_SPI_LP_SPI_WAKEUP_INT interrupt.             |
| 24  | LP_SPI_TRANS_DONE_INT_RAW                  | The raw interrupt status of SPI_TRANS_DONE_INT interrupt.                   |
| 23  | LP_SPI_SLV_WR_BUF_DONE_INT_RAW             | The raw interrupt status of SPI_SLV_WR_BUF_DONE_INT interrupt.              |
| 22  | LP_SPI_SLV_RD_BUF_DONE_INT_RAW             | The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT interrupt.              |
| 21  | (reserved)                                 |                                                                             |
| 20  | LP_SPI_SLV_WRRD_BUF_DONE_INT_RAW           | The raw interrupt status of SPI_SLV_WRD_BUF_DONE_INT interrupt.             |
| 19  | LP_SPI_SLV_WAKEUP_INT_RAW                  | The raw interrupt status of SPI_SLV_WAKEUP_INT interrupt.                   |
| 18  | LP_SPI_MST_RX_AFIFO_WFULL_ERR_INT_RAW      | The raw interrupt status of SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt.        |
| 17  | LP_SPI_MST_TX_AFIFO_REMPTY_ERR_INT_RAW     | The raw interrupt status of SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt.       |
| 16  | LP_SPI_APP1_INT_RAW                        | The raw interrupt status of SPI_APP1_INT interrupt.                         |
| 15  | (reserved)                                 |                                                                             |
| 14  | LP_SPI_SLV_CMD_ERR_INT_RAW                 | The raw interrupt status of SPI_SLV_CMD_ERR_INT interrupt.                  |
| 13  | LP_SPI_SLV_BUF_ADDR_ERR_INT_RAW            | The raw interrupt status of SPI_SLV_BUF_ADDR_ERR_INT interrupt.             |
| 12  | LP_SPI_WAKEUP_INT_RAW                      | The raw interrupt status of LP_SPI_LP_SPI_WAKEUP_INT interrupt.             |
| 11  | LP_SPI_TRANS_DONE_INT_RAW                  | The raw interrupt status of SPI_TRANS_DONE_INT interrupt.                   |
| 10  | LP_SPI_SLV_WR_BUF_DONE_INT_RAW             | The raw interrupt status of SPI_SLV_WR_BUF_DONE_INT interrupt.              |
| 9   | LP_SPI_SLV_RD_BUF_DONE_INT_RAW             | The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT interrupt.              |
| 8   | (reserved)                                 |                                                                             |
| 7   | LP_SPI_APP2_INT_RAW                        | The raw interrupt status of SPI_APP2_INT interrupt.                         |
| 6   | LP_SPI_MST_TX_AFIFO_REMPTY_ERR_INT_RAW     | The raw interrupt status of SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt.       |
| 5   | LP_SPI_MST_RX_AFIFO_WFULL_ERR_INT_RAW      | The raw interrupt status of SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt.        |
| 4   | LP_SPI_SLV_CMD_ERR_INT_RAW                 | The raw interrupt status of SPI_SLV_CMD_ERR_INT interrupt.                  |
| 3   | LP_SPI_SLV_BUF_ADDR_ERR_INT_RAW            | The raw interrupt status of SPI_SLV_BUF_ADDR_ERR_INT interrupt.             |
| 2   | LP_SPI_WAKEUP_INT_RAW                      | The raw interrupt status of LP_SPI_LP_SPI_WAKEUP_INT interrupt.             |
| 1   | LP_SPI_TRANS_DONE_INT_RAW                  | The raw interrupt status of SPI_TRANS_DONE_INT interrupt.                   |
| 0   | Reset                                      | All bits reset to 0.                                                         |

LP_SPI_SLV_RD_BUF_DONE_INT_RAW The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT interrupt.
(R/WTC/SS)

LP_SPI_SLV_WR_BUF_DONE_INT_RAW The raw interrupt status of SPI_SLV_WR_BUF_DONE_INT interrupt.
(R/WTC/SS)

LP_SPI_TRANS_DONE_INT_RAW The raw interrupt status of SPI_TRANS_DONE_INT interrupt.
(R/WTC/SS)

LP_SPI_WAKEUP_INT_RAW The raw interrupt status of LP_SPI_LP_SPI_WAKEUP_INT interrupt.
(R/WTC/SS)

LP_SPI_SLV_BUF_ADDR_ERR_INT_RAW The raw interrupt status of SPI_SLV_BUF_ADDR_ERR_INT interrupt.
(R/WTC/SS)

LP_SPI_SLV_CMD_ERR_INT_RAW The raw interrupt status of SPI_SLV_CMD_ERR_INT interrupt.
(R/WTC/SS)

LP_SPI_MST_RX_AFIFO_WFULL_ERR_INT_RAW The raw interrupt status of SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt.
(R/WTC/SS)

LP_SPI_MST_TX_AFIFO_REMPTY_ERR_INT_RAW The raw interrupt status of SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt.
(R/WTC/SS)

LP_SPI_APP2_INT_RAW The raw interrupt status of SPI_APP2_INT interrupt.
The value is only controlled by the application.
(R/WTC/SS)

LP_SPI_APP1_INT_RAW The raw interrupt status of SPI_APP1_INT interrupt.
The value is only controlled by the application.
(R/WTC/SS)
```