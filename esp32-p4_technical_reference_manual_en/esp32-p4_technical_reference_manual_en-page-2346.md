

```markdown
Register 43.95. LP_SPI_DMA_INT_ENA_REG (0x0034)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | LP_SPI_APP1_INT_ENA | LP_SPI_APP2_INT_ENA | SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ENA | SPI_MST_RX_AFIFO_WFULL_ERR_INT_ENA | (reserved) | LP_SPI_SLV_WR_BUF_DONE_INT_ENA | LP_SPI_SLV_RD_BUF_DONE_INT_ENA | LP_SPI_WAKEUP_INT_ENA | LP_SPI_SLV_BUF_ADDR_ERR_INT_ENA | LP_SPI_SLV_CMD_ERR_INT_ENA |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | SPI_MST_RX_AFIFO_WFULL_ERR_INT_ENA | LP_SPI_SLV_WR_BUF_DONE_INT_ENA | LP_SPI_SLV_RD_BUF_DONE_INT_ENA | LP_SPI_TRANS_DONE_INT_ENA | LP_SPI_WAKEUP_INT_ENA | LP_SPI_SLV_BUF_ADDR_ERR_INT_ENA | LP_SPI_SLV_CMD_ERR_INT_ENA |

LP_SPI_SLV_RD_BUF_DONE_INT_ENA Write 1 to enable SPI_SLV_RD_BUF_DONE_INT interrupt.
(R/W)

LP_SPI_SLV_WR_BUF_DONE_INT_ENA Write 1 to enable SPI_SLV_WR_BUF_DONE_INT interrupt.
(R/W)

LP_SPI_TRANS_DONE_INT_ENA Write 1 to enable SPI_TRANS_DONE_INT interrupt.
(R/W)

LP_SPI_WAKEUP_INT_ENA Write 1 to enable LP_SPI_WAKEUP_INT interrupt.
(R/W)

LP_SPI_SLV_BUF_ADDR_ERR_INT_ENA Write 1 to enable SPI_SLV_BUF_ADDR_ERR_INT interrupt.
(R/W)

LP_SPI_SLV_CMD_ERR_INT_ENA Write 1 to enable SPI_SLV_CMD_ERR_INT interrupt.
(R/W)

LP_SPI_MST_RX_AFIFO_WFULL_ERR_INT_ENA Write 1 to enable
SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt.
(R/W)

LP_SPI_MST_TX_AFIFO_REMPTY_ERR_INT_ENA Write 1 to enable
SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt.
(R/W)

LP_SPI_APP2_INT_ENA Write 1 to enable SPI_APP2_INT interrupt.
(R/W)

LP_SPI_APP1_INT_ENA Write 1 to enable SPI_APP1_INT interrupt.
(R/W)
```