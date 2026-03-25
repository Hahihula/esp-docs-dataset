

```markdown
Register 33.21. SPI_DMA_INT_SET_REG (0x0044)

Continued from the previous page...

SPI_DMA_SEG_TRANS_DONE_INT_SET Write 1 to set the SPI_DMA_SEG_TRANS_DONE_INT interrupt.
(WT)

SPI_SEG_MAGIC_ERR_INT_SET Write 1 to set the SPI_SEG_MAGIC_ERR_INT interrupt.
(WT)

SPI_SLV_BUF_ADDR_ERR_INT_SET Write 1 to set the SPI_SLV_BUF_ADDR_ERR_INT interrupt.
(WT)

SPI_SLV_CMD_ERR_INT_SET Write 1 to set the SPI_SLV_CMD_ERR_INT interrupt.
(WT)

SPI_MST_RX_AFIFO_WFULL_ERR_INT_SET Write 1 to set the SPI_MST_RX_AFIFO_WFULL_ERR_INT interrupt.
(WT)

SPI_MST_TX_AFIFO_REMPTY_ERR_INT_SET Write 1 to set the SPI_MST_TX_AFIFO_REMPTY_ERR_INT interrupt.
(WT)

SPI_APP2_INT_SET Write 1 to set the SPI_APP2_INT interrupt.
(WT)

SPI_APP1_INT_SET Write 1 to set the SPI_APP1_INT interrupt.
(WT)
```

```markdown
Register 33.22. SPI_WO_REG (0x0098)

SPI_BUFO

31 ---------------------------------------------------------- 0
| Reset |
----------------------------------------------------------

SPI_BUFO 32-bit data buffer 1.
(R/W/SS)
```