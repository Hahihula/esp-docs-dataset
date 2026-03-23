

```markdown
|Transfer Type|Communication Mode|Controlled by|Interrupt|
|:--------------|:-------------------|:---------------------------------------------|:---------|
|1 If GDMA_IN_SUC_EOF_CHn_INT is triggered, it means all the RX data has been stored in the RX buffer, and the TX data has been sent to the slave.<br/>2 SPI_TRAN_DONE_INT is triggered when CS is high, which indicates that master has completed the data exchange in SPI_WO_REG ~ SPI_W15_REG with slave in this mode.<br/>3 SPI_SLV_WR_DMA_DONE_INT just means that the transmission on the SPI bus is done, but can not ensure that all the push data has been stored in the RX buffer. For this reason, GDMA_IN_SUC_EOF_CHn_INT is recommended.<br/>4 Or wait for SPI_SLV_WR_BUF_DONE_INT.<br/>5 Or wait for SPI_SLV_RD_DMA_DONE_INT.<br/>6 Or wait for SPI_SLV_RD_BUF_DONE_INT.<br/>7 Slave should set the total read data byte length in SPI_MS_DATA_BITLEN before the transfer begins. Set SPI_RX_EOF_EN to 1 before the end of the interrupt program.<br/>8 Master and slave should define a method to end the segmented transfer, such as via GPIO interrupt.<br/>9 Master sends End_SEG_TRAN to end the segmented transfer or slave sets the total read data byte length in SPI_MS_DATA_BITLEN and waits for GDMA_IN_SUC_EOF_CHn_INT.<br/>10 Half-duplex Wr_BUF single transfer can be used in a slave segmented transfer.<br/>11 Master sends End_SEG_TRAN to end the segmented transfer.<br/>12 Half-duplex Rd_BUF single transfer can be used in a slave segmented transfer.|
|                                                                                                                                      |                                                                                                     ||
```

## 28.10 Register Summary

The addresses in this section are relative to SPI base address provided in Table 5.3-2 in Chapter 5 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.

```markdown
|Name|Description|Address|Access|
|:-----------------------------|:------------------------------------------|:--------|:-------|
|User-defined control registers||||
|SPI_CMD_REG|Command control register|0x0000|varies|
|SPI_ADDR_REG|Address value register|0x0004|R/W|
|SPI_USER_REG|SPI USER control register|0x0010|varies|
|SPI_USER1_REG|SPI USER control register 1|0x0014|R/W|
|SPI_USER2_REG|SPI USER control register 2|0x0018|R/W|
|Control and configuration registers||||
|SPI_CTRL_REG|SPI control register|0x0008|varies|
|SPI_MS_DLEN_REG|SPI data bit length control register|0x001C|R/W|
|SPI_MISC_REG|SPI misc register|0x0020|varies|
|SPI_DMA_CONF_REG|SPI DMA control register|0x0030|varies|
|SPI_SLAVE_REG|SPI slave control register|0x00E0|varies|
|SPI_SLAVE1_REG|SPI slave control register 1|0x00E4|R/W/SS|
|Clock control registers||||
|SPI_CLOCK_REG|SPI clock control register|0x00OC|R/W|
|SPI_CLK_GATE_REG|SPI module clock and register clock control|0x00E8|R/W|
```