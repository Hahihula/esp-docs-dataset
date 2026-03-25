

```markdown
6. Set the polarity of FSPICLK according to Section 26.7.
7. Prepare data according to the selected transfer type:
    * In CPU-controlled MOSI transfer, prepare data in registers SPI_WO_REG~SPI_W15_REG.
    * In DMA-controlled transfer,
        - configure SPI_DMA_TX_ENA/SPI_DMA_RX_ENA,
        - configure GDMA TX/RX link,
        - and start GDMA TX/RX engine, as described in Section 26.5.7 and Section 26.5.8.
8. Configure interrupts and wait for SPI slave to get ready for transfer.
9. Set SPI_DMA_AFIFO_RST, SPI_BUF_AFIFO_RST, and SPI_RX_AFIFO_RST to reset these buffers.
10. Set SPI_USR in register SPI_CMD_REG to start the transfer and wait for the configured interrupts.

Application Example

The following example shows how GP-SPI2 accesses flash and external RAM in master half-duplex communication.

Figure 26.5-7. Connection of GP-SPI2 to Flash and External RAM in 4-bit Mode
```