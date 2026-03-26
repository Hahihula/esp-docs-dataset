

```markdown
Register 43.21. SPI_DMA_INT_SET_REG (0x0044)

Continued from the previous page...

SPI_DMA_SEG_TRANS_DONE_INT_SET Write 1 to set SPI_DMA_SEG_TRANS_DONE_INT interrupt.
(WT)

SPI_SEG_MAGIC_ERR_INT_SET Write 1 to set SPI_SEG_MAGIC_ERR_INT interrupt.
(WT)

SPI_SLV_BUF_ADDR_ERR_INT_SET Write 1 to set SPI_SLV_BUF_ADDR_ERR_INT interrupt.
(WT)

SPI_SLV_CMD_ERR_INT_SET Write 1 to set SPI_SLV_CMD_ERR_INT interrupt.
(WT)

SPI_MST_RX_AFIFO_WFULL_ERR_INT_SET Write 1 to set SPI_MST_RX_AFIFO_WFULL_ERR_INT
interrupt.
(WT)

SPI_MST_TX_AFIFO_REMPTY_ERR_INT_SET Write 1 to set SPI_MST_TX_AFIFO_REMPTY_ERR_INT
interrupt.
(WT)

SPI_APP2_INT_SET Write 1 to set SPI_APP2_INT interrupt.
(WT)

SPI_APP1_INT_SET Write 1 to set SPI_APP1_INT interrupt.
(WT)
```

```markdown
Register 43.22. SPI_WO_REG (0x0098)

[Diagram Description: A horizontal register block labeled "SPI_BUFO" at the bottom left, with a bit field spanning from bit 31 to reset value on the right. The entire width is marked as "Total".]

SPI_BUFO 32-bit data buffer 0.
(R/W/SS)
```