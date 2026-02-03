Title: Chapter 30 SPI Controller (SPI)

Body Text:
In a configurable segmented transfer, the registers of each single transaction (segment) are configurable. This feature enables GP-SPI2 to do as many transactions (segments) as configured after such transfer is triggered once by the CPU. Figure 30.5-9 shows how this feature works.

Figure Caption: 
Figure 30.5-9. Configurable Segmented Transfer in DMA-Controlled Master Mode

Body Text:
As shown in Figure 30.5-9, the registers for one transaction (segment n) can be reconfigured by GP-SPI2 hardware according to the content in its Conf_buf during a CONF state, before this segment starts.

It's recommended to separate GDMA CONF links and CONF buffers (conf_buf) in Figure 30.5-9) for each CONF state. A GDMA TX link is used to connect all the CONF buffers and TX data buffers (Tx_buf) into a chain. Hence, the behavior of the FSPI bus in each segment can be controlled independently.

For example, in a configurable segment transfer, its segment i, segment j, and segment k can be configured to full-duplex, half-duplex MISO, and half-duplex MOSI, respectively. i, j, and k are integer variables, which can be any segment number.

Meanwhile, the state of GP-SPI2, the data length and cycle length of the FSPI bus, and the behavior of the GDMA, can be configured independently for each segment. When this whole DMA-controlled transfer (consisting of several segments) has finished, a GP-SPI2 interrupt, SPI_DMA_SEGTrans_DONE_INT, is triggered.

Subtitle: Configuration

List:
1. Configure the IO path via IOMUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure APB clock (APB_CLK) and module clock (clk_spi_mst) for GP-SPI2 module.
3. Clear SPI_DOUTDIN and SPI_SLAVE_MODE, to enable half-duplex communication in master mode.
4. Configure GP-SPI2 registers listed in Table 30.5-8.
5. Configure SPI CS setup time and hold time according to Section 30.6.
6. Set the property of FSPICLK according to Section 30.7.
7. Prepare descriptors for GDMA CONF buffer and TX data (optional) for each segment. Chain the descriptors of CONF buf and TX buffers of several segments into one linked list.
8. Similarly, prepare descriptors for RX buffers for each segment and chain them into one linked list.

Footer:
Espressif Systems
1132
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)