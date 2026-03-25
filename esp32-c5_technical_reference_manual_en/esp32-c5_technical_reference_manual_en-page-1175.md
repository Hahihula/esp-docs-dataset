

```markdown
Register 33.10. SPI_SLAVE_REG (0x00E0)

Continued from the previous page...

SPI_SLV_WRBUF_BITLEN_EN Configures whether or not to use SPI_SLV_DATA_BITLEN to store the data bit length of Wr_BUF transfer.
O: Not use
1: Use
(R/W)

SPI_SLV_LAST_BYTE_STRE Represents the effective bit of the last received data byte in SPI slave FD and HD mode.
(R/SS)

SPI_DMA_SEG_MAGIC_VALUE Configures the magic value of BM table in DMA-controlled configurable segmented transfer.
(R/W)

SPI_SLAVE_MODE Configures SPI work mode.
O: Master
1: Slave
(R/W)

SPI_SOFT_RESET Configures whether to reset the SPI clock line, CS line, and data line via software.
O: Not reset
1: Reset
Can be configured in CONF state.
(WT)

SPI_USR_CONF Configures whether or not to enable the CONF state of current DMA-controlled configurable segmented transfer.
O: No effect, which means the current transfer is not a configurable segmented transfer.
1: Enable, which means a configurable segmented transfer is started.
(R/W)

SPI_MST_FD_WAIT_DMA_TX_DATA Configures whether or not to wait DMA TX data gets ready before starting SPI transfer in master full-duplex transfer.
O: Not wait
1: Wait
(R/W)
```