

```markdown
## 29.9 Interrupts

### Interrupt Summary

GP-SPI2 provides an SPI interface interrupt `SPI_INTR`. When an SPI transfer ends, an interrupt is generated in GP-SPI2.

*   `SPI_DMA_INFIFO_FULL_ERR_INT`: triggered when the length of GDMA RX FIFO is shorter than that of actual data transferred.
*   `SPI_DMA_OUTFIFO_EMPTY_ERR_INT`: triggered when the length of GDMA TX FIFO is shorter than that of actual data transferred.
*   `SPI_SLV_EX_QPI_INT`: triggered when Ex_QPI is received correctly in GP-SPI2 as slave and the SPI transfer ends.
*   `SPI_SLV_EN_QPI_INT`: triggered when En_QPI is received correctly in GP-SPI2 as slave and the SPI transfer ends.
*   `SPI_SLV_CMD7_INT`: triggered when CMD7 is received correctly in GP-SPI2 as slave and the SPI transfer ends.
*   `SPI_SLV_CMD8_INT`: triggered when CMD8 is received correctly in GP-SPI2 as slave and the SPI transfer ends.
*   `SPI_SLV_CMD9_INT`: triggered when CMD9 is received correctly in GP-SPI2 as slave and the SPI transfer ends.
*   `SPI_SLV_CMDA_INT`: triggered when CMDA is received correctly in GP-SPI2 as slave and the SPI transfer ends.
*   `SPI_SLV_RD_DMA_DONE_INT`: triggered at the end of Rd_DMA transfer as slave.
*   `SPI_SLV_WR_DMA_DONE_INT`: triggered at the end of Wr_DMA transfer as slave.
*   `SPI_SLV_RD_BUF_DONE_INT`: triggered at the end of Rd_BUF transfer as slave.
*   `SPI_SLV_WR_BUF_DONE_INT`: triggered at the end of Wr_BUF transfer as slave.
*   `SPI_TRANS_DONE_INT`: triggered at the end of SPI bus transfer in both as master and as slave.
```