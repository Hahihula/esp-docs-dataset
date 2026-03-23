

```markdown
Register 28.10. SPI_SLAVE_REG (0x00E0)

Continued from the previous page...

SPI_SLV_RDBUF_BITLEN_EN Configures whether or not to use `SPI_SLV_DATA_BITLEN` to store the data bit length of Rd_BUF transfer. (R/W)
*   0: Not use
*   1: Use

SPI_SLV_WRBUF_BITLEN_EN Configures whether or not to use `SPI_SLV_DATA_BITLEN` to store the data bit length of Wr_BUF transfer. (R/W)
*   0: Not use
*   1: Use

SPI_DMA_SEG_MAGIC_VALUE Configures the magic value of BM table in DMA-controlled configurable segmented transfer. (R/W)

SPI_SLAVE_MODE Configures SPI work mode. (R/W)
*   0: Master
*   1: Slave

SPI_SOFT_RESET Configures whether to reset the SPI clock line, CS line, and data line via software. (WT)
*   0: Not reset
*   1: Reset

Can be configured in CONF state.

SPI_USR_CONF Configures whether or not to enable the CONF state of current DMA-controlled configurable segmented transfer. (R/W)
*   0: No effect, which means the current transfer is not a configurable segmented transfer.
*   1: Enable, which means a configurable segmented transfer is started.

SPI_MST_FD_WAIT_DMA_TX_DATA Configures whether or not to wait DMA TX data gets ready before starting SPI transfer in master full-duplex transfer. (R/W)
*   0: Not wait
*   1: Wait
```