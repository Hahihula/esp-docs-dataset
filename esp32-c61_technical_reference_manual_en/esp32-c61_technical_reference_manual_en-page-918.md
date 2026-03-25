

```markdown
|Internal Interrupt Source|Trigger Condition|Interrupt Signal|
|:--------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------|
|SPI_DMA_INFIFO_FULL_ERR_INT|The length of GDMA RX FIFO is shorter than that of actual data transferred|SPI_INTR|
|SPI_DMA_OUTFIFO_EMPTY_ERR_INT|The length of GDMA TX FIFO is shorter than that of actual data transferred|SPI_INTR|
|SPI_SLV_EX_QPI_INT|Ex_QPI is received correctly when GP-SPI2 works as slave and the SPI transfer ends|SPI_INTR|
|SPI_SLV_EN_QPI_INT|En_QPI is received correctly when GP-SPI2 works as slave and the SPI transfer ends|SPI_INTR|
|SPI_SLV_CMD7_INT|CMD7 is received correctly when GP-SPI2 works as slave and the SPI transfer ends|SPI_INTR|
|SPI_SLV_CMD8_INT|CMD8 is received correctly when GP-SPI2 works as slave and the SPI transfer ends|SPI_INTR|
|SPI_SLV_CMD9_INT|CMD9 is received correctly when GP-SPI2 works as slave and the SPI transfer ends|SPI_INTR|
|SPI_SLV_CMDA_INT|CMDA is received correctly when GP-SPI2 works as slave and the SPI transfer ends|SPI_INTR|
|SPI_SLV_RD_DMA_DONE_INT|At the end of Rd_DMA transfer when GP-SPI2 works as slave|SPI_INTR|
|SPI_SLV_WR_DMA_DONE_INT|At the end of Wr_DMA transfer when GP-SPI2 works as slave|SPI_INTR|
|SPI_SLV_RD_BUF_DONE_INT|At the end of Rd_BUF transfer when GP-SPI2 works as slave|SPI_INTR|
|SPI_SLV_WR_BUF_DONE_INT|At the end of Wr_BUF transfer when GP-SPI2 works as slave|SPI_INTR|
|SPI_TRANS_DONE_INT|At the end of SPI bus transfer when GP-SPI2 works as master or as slave|SPI_INTR|
```