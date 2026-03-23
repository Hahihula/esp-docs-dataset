

```markdown
Register 28.19. SPI_DMA_INT_RAW_REG (0x003C)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                 | (reserved)                                                                  |
| 30  | SPI_APP1_INT_RAW                | The raw interrupt status of SPI_APP1_INT interrupt.                         |
| 29  | SPI_APP2_INT_RAW                | The raw interrupt status of SPI_APP2_INT interrupt.                         |
| 28  | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_RAW | The raw interrupt status of SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt.      |
| 27  | SPI_MST_RX_AFIFO_FULL_ERR_INT_RAW | The raw interrupt status of SPI_MST_RX_AFIFO_FULL_ERR_INT interrupt.        |
| 26  | (reserved)                     |                                                                             |
| 25  | SPI_SLV_CMD_ERR_INT_RAW         | The raw interrupt status of SPI_SLV_CMD_ERR_INT interrupt.                  |
| 24  | SPI_DMA_MAGIC_ERR_INT_RAW       | The raw interrupt status of SPI_DMA_MAGIC_ERR_INT interrupt.                |
| 23  | SPI_DTRA_SEG_TRANS_DONE_RAW     | The raw interrupt status of SPI_DTRA_SEG_TRANS_DONE interrupt.              |
| 22  | SPI_SLV_RDR_DONE_INT_RAW        | The raw interrupt status of SPI_SLV_RDR_DONE_INT interrupt.                 |
| 21  | SPI_SLV_WR_DONE_INT_RAW         | The raw interrupt status of SPI_SLV_WR_DONE_INT interrupt.                  |
| 20  | SPI_SLV_RD_BUF_DONE_INT_RAW     | The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT interrupt.              |
| 19  | SPI_SLV_WR_BUF_DONE_INT_RAW     | The raw interrupt status of SPI_SLV_WR_BUF_DONE_INT interrupt.              |
| 18  | SPI_TRANS_DONE_INT_RAW          | The raw interrupt status of SPI_TRANS_DONE_INT interrupt.                   |
| 17  | SPI_SLV_EX_QPI_INT_RAW          | The raw interrupt status of SPI_SLV_EX_QPI_INT interrupt.                   |
| 16  | SPI_SLV_EN_QPI_INT_RAW          | The raw interrupt status of SPI_SLV_EN_QPI_INT interrupt.                   |
| 15  | SPI_SLV_CMD7_INT_RAW            | The raw interrupt status of SPI_SLV_CMD7_INT interrupt.                     |
| 14  | SPI_SLV_CMD8_INT_RAW            | The raw interrupt status of SPI_SLV_CMD8_INT interrupt.                     |
| 13  | SPI_SLV_CMD9_INT_RAW            | The raw interrupt status of SPI_SLV_CMD9_INT interrupt.                     |
| 12  | SPI_SLV_CMDA_INT_RAW            | The raw interrupt status of SPI_SLV_CMDA_INT interrupt.                     |
| 11  | SPI_SLV_RD_DMA_DONE_INT_RAW     | The raw interrupt status of SPI_SLV_RD_DMA_DONE_INT interrupt.              |
| 10  | SPI_SLV_WR_DMA_DONE_INT_RAW     | The raw interrupt status of SPI_SLV_WR_DMA_DONE_INT interrupt.              |
| 9   |                                 |                                                                             |
| 8-0 | Reset                           | All bits reset to 0                                                           |

SPI_DMA_INFIFO_FULL_ERR_INT_RAW    The raw interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT interrupt. (R/WTC/SS)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW  The raw interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT interrupt. (R/WTC/SS)

SPI_SLV_EX_QPI_INT_RAW             The raw interrupt status of SPI_SLV_EX_QPI_INT interrupt. (R/WTC/SS)

SPI_SLV_EN_QPI_INT_RAW             The raw interrupt status of SPI_SLV_EN_QPI_INT interrupt. (R/WTC/SS)

SPI_SLV_CMD7_INT_RAW               The raw interrupt status of SPI_SLV_CMD7_INT interrupt. (R/WTC/SS)

SPI_SLV_CMD8_INT_RAW               The raw interrupt status of SPI_SLV_CMD8_INT interrupt. (R/WTC/SS)

SPI_SLV_CMD9_INT_RAW               The raw interrupt status of SPI_SLV_CMD9_INT interrupt. (R/WTC/SS)

SPI_SLV_CMDA_INT_RAW               The raw interrupt status of SPI_SLV_CMDA_INT interrupt. (R/WTC/SS)

SPI_SLV_RD_DMA_DONE_INT_RAW        The raw interrupt status of SPI_SLV_RD_DMA_DONE_INT interrupt. (R/WTC/SS)

SPI_SLV_WR_DMA_DONE_INT_RAW        The raw interrupt status of SPI_SLV_WR_DMA_DONE_INT interrupt. (R/WTC/SS)

SPI_SLV_RD_BUF_DONE_INT_RAW        The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT interrupt. (R/WTC/SS)

SPI_SLV_WR_BUF_DONE_INT_RAW        The raw interrupt status of SPI_SLV_WR_BUF_DONE_INT interrupt. (R/WTC/SS)

SPI_TRANS_DONE_INT_RAW             The raw interrupt status of SPI_TRANS_DONE_INT interrupt. (R/WTC/SS)

Continued on the next page...
```