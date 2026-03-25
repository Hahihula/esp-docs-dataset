

```markdown
Register 33.19. SPI_DMA_INT_RAW_REG (0x003C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | SPI_APP1_INT_RAW               | The raw interrupt status of SPI_APP1_INT.                                   |
| 29  | SPI_APP2_INT_RAW               | The raw interrupt status of SPI_APP2_INT.                                   |
| 28  | SPI_MST_TX_AFIFO_ERRP_INT_RAW | The raw interrupt status of SPI_MST_TX_AFIFO_ERRP_INT.                      |
| 27  | SPI_MST_RX_AFIFO_ERRP_INT_RAW | The raw interrupt status of SPI_MST_RX_AFIFO_ERRP_INT.                      |
| 26  | SPI_SLV_CMD_ERRP_INT_RAW      | The raw interrupt status of SPI_SLV_CMD_ERRP_INT.                           |
| 25  | SPI_SEG_DONE_INT_RAW           | The raw interrupt status of SPI_SEG_DONE_INT.                               |
| 24  | SPI_DMA_SLR_DONE_INT_RAW       | The raw interrupt status of SPI_DMA_SLR_DONE_INT.                           |
| 23  | SPI_SLV_RDR_DONE_INT_RAW       | The raw interrupt status of SPI_SLV_RDR_DONE_INT.                           |
| 22  | SPI_SLV_WRD_DONE_INT_RAW       | The raw interrupt status of SPI_SLV_WRD_DONE_INT.                           |
| 21  | SPI_SLV_CMD9_INT_RAW           | The raw interrupt status of SPI_SLV_CMD9_INT.                               |
| 20  | SPI_SLV_CMD8_INT_RAW           | The raw interrupt status of SPI_SLV_CMD8_INT.                               |
| 19  | SPI_SLV_EX_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EX_QPI_INT.                             |
| 18  | SPI_SLV_EN_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EN_QPI_INT.                             |
| 17  | SPI_SLV_CMD7_INT_RAW           | The raw interrupt status of SPI_SLV_CMD7_INT.                               |
| 16  | SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW | The raw interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT.                |
| 15  | SPI_DMA_INFIFO_FULL_ERR_INT_RAW | The raw interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT.                   |
| 14  | SPI_SLV_CMD6_INT_RAW           | The raw interrupt status of SPI_SLV_CMD6_INT.                               |
| 13  | SPI_SLV_CMD5_INT_RAW           | The raw interrupt status of SPI_SLV_CMD5_INT.                               |
| 12  | SPI_SLV_CMD4_INT_RAW           | The raw interrupt status of SPI_SLV_CMD4_INT.                               |
| 11  | SPI_SLV_CMD3_INT_RAW           | The raw interrupt status of SPI_SLV_CMD3_INT.                               |
| 10  | SPI_SLV_CMD2_INT_RAW           | The raw interrupt status of SPI_SLV_CMD2_INT.                               |
| 9   | SPI_SLV_CMD1_INT_RAW           | The raw interrupt status of SPI_SLV_CMD1_INT.                               |
| 8   | SPI_SLV_CMD0_INT_RAW           | The raw interrupt status of SPI_SLV_CMD0_INT.                               |
| 7   | SPI_SLV_WRD_DONE_INT_RAW       | The raw interrupt status of SPI_SLV_WRD_DONE_INT.                           |
| 6   | SPI_SLV_RDR_DONE_INT_RAW       | The raw interrupt status of SPI_SLV_RDR_DONE_INT.                           |
| 5   | SPI_SLV_CMD9_INT_RAW           | The raw interrupt status of SPI_SLV_CMD9_INT.                               |
| 4   | SPI_SLV_CMD8_INT_RAW           | The raw interrupt status of SPI_SLV_CMD8_INT.                               |
| 3   | SPI_SLV_EX_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EX_QPI_INT.                             |
| 2   | SPI_SLV_EN_QPI_INT_RAW         | The raw interrupt status of SPI_SLV_EN_QPI_INT.                             |
| 1   | SPI_SLV_CMD7_INT_RAW           | The raw interrupt status of SPI_SLV_CMD7_INT.                               |
| 0   | Reset                          | Reset value for the register                                                  |

SPI_DMA_INFIFO_FULL_ERR_INT_RAW    The raw interrupt status of SPI_DMA_INFIFO_FULL_ERR_INT.
(R/WTC/SS)

SPI_DMA_OUTFIFO_EMPTY_ERR_INT_RAW  The raw interrupt status of SPI_DMA_OUTFIFO_EMPTY_ERR_INT.

SPI_SLV_EX_QPI_INT_RAW              The raw interrupt status of SPI_SLV_EX_QPI_INT.
(R/WTC/SS)

SPI_SLV_EN_QPI_INT_RAW              The raw interrupt status of SPI_SLV_EN_QPI_INT.
(R/WTC/SS)

SPI_SLV_CMD7_INT_RAW                The raw interrupt status of SPI_SLV_CMD7_INT.
(R/WTC/SS)

SPI_SLV_CMD8_INT_RAW                The raw interrupt status of SPI_SLV_CMD8_INT.
(R/WTC/SS)

SPI_SLV_CMD9_INT_RAW                The raw interrupt status of SPI_SLV_CMD9_INT.
(R/WTC/SS)

SPI_SLV_CMDA_INT_RAW                The raw interrupt status of SPI_SLV_CMDA_INT.
(R/WTC/SS)

SPI_SLV_RD_DMA_DONE_INT_RAW         The raw interrupt status of SPI_SLV_RD_DMA_DONE_INT.
(R/WTC/SS)

SPI_SLV_WR_DMA_DONE_INT_RAW         The raw interrupt status of SPI_SLV_WR_DMA_DONE_INT.
(R/WTC/SS)

SPI_SLV_RD_BUF_DONE_INT_RAW         The raw interrupt status of SPI_SLV_RD_BUF_DONE_INT.
(R/WTC/SS)

Continued on the next page...
```