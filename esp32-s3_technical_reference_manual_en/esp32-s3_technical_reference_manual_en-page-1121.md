Title: Chapter 30 SPI Controller (SPI)

Figure Caption:
- Figure 30.5-4 shows the data flow in GP-SPI slave mode.

Body Text:

1. In CPU/DMA-controlled full-duplex/half-duplex modes, when an external SPI master starts the SPI transfer, data on the FSPI/SPI3 bus is captured, converted into unit of bytes by spi_slv_din_ctrl module, and then is stored in spi_rx_affo.

2. - In CPU-controlled full-duplex transfer, the received data in spi_rx_affo will be later stored into registers SPI_WO_REG ~ SPI_W15_REG, successively.
- In half-duplex Wr BUFFER transfer, when the value of address (SLV_ADDR[7:0]) is received, the received data in spi_rx_affo will be stored in the related address of registers SPI_WO_REG ~ SPI_W15_REG.

3. - In DMA-controlled full-duplex transfer or in half-duplex Wr DMA transfer, the received data in spi_rx_affo will be stored in the configured GDMA RX buffer.
- In CPU-controlled full-/half-duplex transfer, the data to send is stored in buf_tx_affo. In DMA-controlled full-/half-duplex transfer, the data to send is stored in dma tx_affo. Therefore, Rd BUFFER transaction controlled by CPU and Rd DMA transaction controlled by DMA can be done in one slave segmented transfer. TX data comes from corresponding addresses according to the transfer modes.
  - In CPU-controlled full-duplex transfer, when SPI_SLAVE_MODE and SPI_DOUTDIN are set and SPI_DMA _TX_ENA is cleared, the data in SPI_WO_REG ~ SPI_W15_REG will be stored into buf tx_affo.

4. - In CPU-controlled half-duplex transfer, when SPI_SLAVE_MODE is set, SPI_DOUTDIN is cleared, Rd BUFFER command and SLV_ADDR[7:0] are received, the data started from the related address of SPI_WO_REG ~ SPI_W15_REG will be stored into buf tx_affo.
- In DMA-controlled full-duplex transfer, when SPI_SLAVE_MODE, SPI_DOUTDIN and SPI_DMA_TX_ENA are set, the data in the configured GDMA TX buffer will be stored into dma tx_affo.

5. - In DMA-controlled half-duplex transfer, when SPI_SLAVE_MODE is set, SPI_DOUTDIN is cleared, and Rd DMA command is received, the data in the configured GDMA TX buffer will be stored into dma tx_affo.
- The data in buf tx_affo or dma tx_affo is sent out by spi_slv_dout_ctrl module in 1/2/4-bit modes.

Subtitle:
30.5.8 GP-SPI Works as a Master

Body Text:

GP-SPI can be configured as a SPI master by clearing the bit SPI_SLAVE_MODE in SPI_SLAVE_REG. In this operation mode, GP-SPI provides clock signal (the divided clock from GP-SPI module clock) and six CS lines (CSO ~ CS5).

Note:
- The length of transferred data must be in unit of bytes, otherwise the extra bits will be lost. The extra bits here means the result of total data bits % 8.
- To transfer bits not in unit of bytes, consider implementing it in CMD state or ADDR state.

Footer: Espressif Systems | Submit Documentation Feedback

Page Number and Document Version:
1121 ESP32-S3 TRM (Version 1.7)