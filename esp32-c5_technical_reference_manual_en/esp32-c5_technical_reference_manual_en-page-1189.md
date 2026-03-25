

```markdown
Register 33.20. SPI_DMA_INT_ST_REG (0x0040)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | SPI_APP1_INT_ST                |                                                                             |
| 29  | SPI_APP2_INT_ST                |                                                                             |
| 28  | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ST | The interrupt status of SPI_MST_TX_AFIFO_REMPTY_ERR_INT.                  |
| 27  | SPI_MST_RX_AFIFO_WFFULL_ERR_INT_ST | The interrupt status of SPI_MST_RX_AFIFO_WFFULL_ERR_INT.                 |
| 26  | SPI_SLV_CMD_ERR_INT_ST        |                                                                             |
| 25  | SPI_SLV_BUF_ADDR_ERR_INT_ST   |                                                                             |
| 24  | SPI_SEG_MAGIC_SECS_TRAN_DONE_INT_ST | The interrupt status of SPI_SEG_MAGIC_SECS_TRAN_DONE_INT.              |
| 23  | SPI_DMA_TRAN_DONE_INT_ST      |                                                                             |
| 22  | SPI_SLV_WR_BUF_DONE_INT_ST    |                                                                             |
| 21  | SPI_SLV_RD_DMA_DONE_INT_ST    |                                                                             |
| 20  | SPI_SLV_CMD9_INT_ST            | The interrupt status of SPI_SLV_CMD9_INT.                                |
| 19  | SPI_SLV_CMD8_INT_ST            | The interrupt status of SPI_SLV_CMD8_INT.                                |
| 18  | SPI_SLV_CMD7_INT_ST            | The interrupt status of SPI_SLV_CMD7_INT.                                |
| 17  | SPI_SLV_EX_QPI_INT_ST          | (RO) The interrupt status of SPI_SLV_EX_QPI_INT.                         |
| 16  | SPI_SLV_EN_QPI_INT_ST          | (RO) The interrupt status of SPI_SLV_EN_QPI_INT.                         |
| 15  | SPI_DMA_OUTFIFO_FULL_ERR_INT_ST | (RO) The interrupt status of SPI_DMA_OUTFIFO_FULL_ERR_INT.               |
| 14  | SPI_DMA_INFIFO_FULL_ERR_INT_ST | (RO) The interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT.                 |
| 13  |                                |                                                                             |
| 12  |                                |                                                                             |
| 11  |                                |                                                                             |
| 10  |                                |                                                                             |
| 9   |                                |                                                                             |
| 8   |                                |                                                                             |
| 7   | SPI_SLV_WR_BUF_DONE_INT_ST    | The interrupt status of SPI_SLV_WR_BUF_DONE_INT.                         |
| 6   | SPI_SLV_RD_BUF_DONE_INT_ST    | The interrupt status of SPI_SLV_RD_BUF_DONE_INT.                         |
| 5   |                                |                                                                             |
| 4   |                                |                                                                             |
| 3   |                                |                                                                             |
| 2   |                                |                                                                             |
| 1   |                                |                                                                             |
| 0   | Reset                          |                                                                             |

SPI_DMA_INFIFO_FULL_ERR_INT_ST The interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT. (RO)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_ST The interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT. (RO)

SPI_SLV_EX_QPI_INT_ST The interrupt status of SPI_SLV_EX_QPI_INT. (RO)

SPI_SLV_EN_QPI_INT_ST The interrupt status of SPI_SLV_EN_QPI_INT. (RO)

SPI_SLV_CMD7_INT_ST The interrupt status of SPI_SLV_CMD7_INT. (RO)

SPI_SLV_CMD8_INT_ST The interrupt status of SPI_SLV_CMD8_INT. (RO)

SPI_SLV_CMD9_INT_ST The interrupt status of SPI_SLV_CMD9_INT. (RO)

SPI_SLV_CMDA_INT_ST The interrupt status of SPI_SLV_CMDA_INT. (RO)

SPI_SLV_RD_DMA_DONE_INT_ST The interrupt status of SPI_SLV_RD_DMA_DONE_INT. (RO)

SPI_SLV_WR_DMA_DONE_INT_ST The interrupt status of SPI_SLV_WR_DMA_DONE_INT. (RO)

SPI_SLV_RD_BUF_DONE_INT_ST The interrupt status of SPI_SLV_RD_BUF_DONE_INT. (RO)

SPI_SLV_WR_BUF_DONE_INT_ST The interrupt status of SPI_SLV_WR_BUF_DONE_INT. (RO)

Continued on the next page...
```