

```markdown
## Figure 43.5-9. Configurable Segmented Transfer as Master

As shown in Figure 43.5-9, the registers for one transaction (segment n) can be reconfigured by GP-SPI2 hardware according to the content in its Conf_bufn during the CONF state, before this segment starts.

It is recommended to provide separate DMA CONF links and CONF buffers (Conf_bufi in Figure 43.5-9) for each CONF state. A DMA TX link is used to connect all the CONF buffers and TX data buffers (Tx_bufi in Figure 43.5-9) into a chain. Hence, the behavior of the SPI2 bus in each segment can be controlled independently.

For example, in a configurable segmented transfer, its segment i, segment j, and segment k can be configured to full-duplex, half-duplex MISO, and half-duplex MOSI, respectively. i, j, and k represent different segment numbers.

Meanwhile, the state of GP-SPI2, the data length and cycle length of the SPI2 bus, and the behavior of the DMA, can be configured independently for each segment. When this whole DMA-controlled transfer (consisting of several segments) has finished, a GP-SPI2 interrupt, SPI_DMA_SEG_TRANS_DONE_INT, is triggered.

### Configuration

1. Configure the IO path via HP IO MUX or HP GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure AHB clock (AHB_CLK) and module clock (clk_spi_mst) for the GP-SPI2 module.
3. Clear SPI_DOUTDIN and SPI_SLAVE_MODE, to enable master half-duplex communication.
4. Configure GP-SPI2 registers listed in Table 43.5-10.
5. Configure SPI CS setup time and hold time according to Section 43.6.
6. Set the property of SPI2CLK according to Section 43.7.
7. Prepare descriptors for DMA CONF buffer and TX data (optional) for each segment. Chain the descriptors of CONF buffer and TX buffers of several segments into one linked list.
8. Similarly, prepare descriptors for RX buffers for each segment and chain them into one linked list.
```