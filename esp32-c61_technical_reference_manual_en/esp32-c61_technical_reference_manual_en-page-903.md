

```markdown
Figure 26.5-9) into a chain. Hence, the behavior of the FSPI bus in each segment can be controlled independently.

For example, in a configurable segmented transfer, its segment i, segment j, and segment k can be configured to full-duplex, half-duplex MISO, and half-duplex MOSI, respectively. i, j, and k represent different segment numbers.

Meanwhile, the state of GP-SPI2, the data length and cycle length of the FSPI bus, and the behavior of the GDMA, can be configured independently for each segment. When this whole DMA-controlled transfer (consisting of several segments) has finished, a GP-SPI2 interrupt, SPI_DMA_SEG_TRANS_DONE_INT, is triggered.

Configuration

1. Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure AHB_CLK, APB_CLK, and module clock (clk_spi_mst) for the GP-SPI2 module.
3. Clear SPI_DOUTDIN and SPI_SLAVE_MODE, to enable master half-duplex communication.
4. Configure GP-SPI2 registers listed in Table 26.5-7.
5. Configure SPI CS setup time and hold time according to Section 26.6.
6. Set the polarity of FSPICLK according to Section 26.7.
7. Prepare descriptors for GDMA CONF buffer and TX data (optional) for each segment. Chain the descriptors of CONF buffer and TX buffers of several segments into one linked list.
8. Similarly, prepare descriptors for RX buffers for each segment and chain them into one linked list.
9. Configure all the needed CONF buffers, TX buffers and RX buffers, respectively for each segment before this DMA-controlled transfer begins.
10. Point AXI_DMA_OUTLINK_ADDR_CHn to the head address of the CONF and TX buffer descriptor linked list, and then set AXI_DMA_OUTLINK_START_CHn to start the TX GDMA.
11. Clear the bit SPI_RX_EOF_EN in register SPI_DMA_CONF_REG. Point AXI_DMA_INLINK_ADDR_CHn to the head address of the CONF and RX buffer descriptor linked list, and then set AXI_DMA_INLINK_START_CHn to start the RX GDMA.
12. Set SPI_USR_CONF to enable CONF state.
13. Set SPI_DMA_SEG_TRANS_DONE_INT_ENA to enable the SPI_DMA_SEG_TRANS_DONE_INT interrupt. Configure other interrupts if needed according to Section 26.9.
14. Wait for all the slaves to get ready for transfer.
15. Set SPI_DMA_AFIFO_RST, SPI_BUF_AFIFO_RST, and SPI_RX_AFIFO_RST to reset these buffers.
16. Set SPI_USR to start this DMA-controlled transfer.
17. Wait for SPI_DMA_SEG_TRANS_DONE_INT interrupt, which means this transfer has finished and the data has been stored into corresponding memory.

Note:
Prepare the data to send for each segment in its PREP state. Shall ensure that:
(SPI_CS_SETUP_TIME + 1) × T_SPI_CLK >= 4 × (TAHB_CLK + Tclk_spi_mst)
```