

```markdown
Register 43.57. SPI_DMA_INT_RAW_REG (0x003C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | SPI_APP1_INT_RAW               | The raw interrupt status of SPI_APP1_INT.                                   |
| 29  | SPI_APP2_INT_RAW               | The raw interrupt status of SPI_APP2_INT.                                   |
| 28  | SPI_MST_TX_AFPO_REMPTY_ERR_INT_RAW | The raw interrupt status of SPI_MST_TX_AFPO_REMPTY_ERR_INT.                |
| 27  | SPI_SLV_CMD_ERR_INT_RAW       | The raw interrupt status of SPI_SLV_CMD_ERR_INT.                            |
| 26  | SPI_SLV_BUF_ADDR_ERR_INT_RAW  | The raw interrupt status of SPI_SLV_BUF_ADDR_ERR_INT.                       |
| 25  | (reserved)                    |                                                                             |
| 24  | SPI_DMA_SEFG_TRANS_DONE_INT_RAW | The raw interrupt status of SPI_DMA_SEFG_TRANS_DONE_INT.                   |
| 23  | SPI_SLV_WR_RDMR_DONE_INT_RAW   | The raw interrupt status of SPI_SLV_WR_RDMR_DONE_INT.                       |
| 22  | SPI_SLV_RD_BUF_DONE_INT_RAW    | The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT.                        |
| 21  | SPI_SLV_CMD9_INT_RAW           | The raw interrupt status of SPI_SLV_CMD9_INT.                               |
| 20  | SPI_SLV_CMD8_INT_RAW           | The raw interrupt status of SPI_SLV_CMD8_INT.                               |
| 19  | SPI_SLV_EN_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EN_QPI_INT.                             |
| 18  | SPI_SLV_EX_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EX_QPI_INT.                             |
| 17  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW | The raw interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT.                |
| 16  | SPI_DMA_INFIFO_FULL_ERR_INT_RAW | The raw interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT.                   |
| 15  |                                |                                                                             |
| 14  | SPI_SLV_CMD7_INT_RAW           | The raw interrupt status of SPI_SLV_CMD7_INT.                               |
| 13  | SPI_SLV_CMD9_INT_RAW           | The raw interrupt status of SPI_SLV_CMD9_INT.                               |
| 12  | SPI_SLV_CMD8_INT_RAW           | The raw interrupt status of SPI_SLV_CMD8_INT.                               |
| 11  | SPI_SLV_EN_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EN_QPI_INT.                             |
| 10  | SPI_SLV_EX_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EX_QPI_INT.                             |
| 9   | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW | The raw interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT.                |
| 8   | SPI_DMA_INFIFO_FULL_ERR_INT_RAW | The raw interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT.                   |
| 7   |                                |                                                                             |
| 6   | SPI_SLV_CMD9_INT_RAW           | The raw interrupt status of SPI_SLV_CMD9_INT.                               |
| 5   | SPI_SLV_CMD8_INT_RAW           | The raw interrupt status of SPI_SLV_CMD8_INT.                               |
| 4   | SPI_SLV_EN_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EN_QPI_INT.                             |
| 3   | SPI_SLV_EX_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EX_QPI_INT.                             |
| 2   |                                |                                                                             |
| 1   | Reset                          |                                                                             |
| 0   |                                |                                                                             |

SPI_DMA_INFIFO_FULL_ERR_INT_RAW    The raw interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT. (R/WTC/SS)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW  The raw interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT. (R/WTC/SS)

SPI_SLV_EX_QPI_INT_RAW              The raw interrupt status of SPI_SLV_EX_QPI_INT. (R/WTC/SS)

SPI_SLV_EN_QPI_INT_RAW              The raw interrupt status of SPI_SLV_EN_QPI_INT. (R/WTC/SS)

SPI_SLV_CMD7_INT_RAW                The raw interrupt status of SPI_SLV_CMD7_INT. (R/WTC/SS)

SPI_SLV_CMD8_INT_RAW                The raw interrupt status of SPI_SLV_CMD8_INT. (R/WTC/SS)

SPI_SLV_CMD9_INT_RAW                The raw interrupt status of SPI_SLV_CMD9_INT. (R/WTC/SS)

SPI_SLV_CMD4_INT_RAW                The raw interrupt status of SPI_SLV_CMD4_INT. (R/WTC/SS)

SPI_SLV_RD_DMA_DONE_INT_RAW         The raw interrupt status of SPI_SLV_RD_DMA_DONE_INT. (R/WTC/SS)

SPI_SLV_WR_DMA_DONE_INT_RAW         The raw interrupt status of SPI_SLV_WR_DMA_DONE_INT. (R/WTC/SS)

SPI_SLV_RD_BUF_DONE_INT_RAW         The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT. (R/WTC/SS)
```