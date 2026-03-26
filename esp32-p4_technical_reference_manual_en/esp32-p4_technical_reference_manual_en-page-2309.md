
```markdown
Register 43.48. SPI_SLAVE_REG (0x00E0)

Continued from the previous page...

SPI_SLV_WRBUF_BITLEN_EN Configures whether or not to use SPI_SLV_DATA_BITLEN to store the data bit length of Wr_BUF transfer.
O: Not use
1: Use
(R/W)

SPI_SLV_LAST_BYTE_STRB Represents the valid bits of the last received data byte in SPI slave full-duplex and half-duplex transfer.
(R/SS)

SPI_SLAVE_MODE Configures SPI work mode.
O: Master
1: Slave
(R/W)

SPI_SOFT_RESET Configures whether to reset the SPI clock line, CS line, and data line via software.
O: Not reset
1: Reset
(WT)

SPI_MST_FD_WAIT_DMA_TX_DATA Configures whether or not to wait DMA TX data gets ready before starting SPI transfer in master full-duplex transfer.
O: Not wait
1: Wait
(R/W)
```