**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Register Information:**
- **Register Name:** Register 30.10. SPI_DMA_CONF_REG (0x003C)
- **Description:** This register is used to configure the DMA operations for the SPI controller.

**Bit Description Table:**

| Bit | Description |
|-----|-------------|
| 31  | Reserved    |
| 30  | Reserved    |
| 29  | Reserved    |
| 28  | Reserved    |
| 27  | Reserved    |
| 26  | Reserved    |
| 25  | Reserved    |
| 24  | Reserved    |
| 23  | Reserved    |
| 22  | Reserved    |
| 21  | Reserved    |
| 20  | Reserved    |
| 19  | Reserved    |
| 18  | Reserved    |
| 17  | Reserved    |
| 16  | Reserved    |
| 15  | Reserved    |
| 14  | Reserved    |
| 13  | Reserved    |
| 12  | Reserved    |
| 11  | Reserved    |
| 10  | Reserved    |
| 9   | Reserved    |
| 8   | Reserved    |
| 7   | Reserved    |
| 6   | Reserved    |
| 5   | Reserved    |
| 4   | Reserved    |
| 3   | Reserved    |
| 2   | Reserved    |
| 1   | Reserved    |
| 0   | Reserved    |

**Bit Values:**
- The bit values are shown as binary numbers (e.g., "0000 0000 0000 0000") with the corresponding register name and description.

**Descriptions for Specific Bits in Register SPI_DMA_CONF_REG:**

1. **SPI_DMA_AFIRO_RST**
   - Description:
     - Set this bit to reset buf_tx_aiffo as shown in Figure 30.5-3.
     - buf_tx_aiffo is used to send data out in CPU-controlled master and slave transfer.

2. **SPI_DMA_RX_ENA**
   - Description: 
     - Set this bit to enable DMA-controlled receive data mode (R/W).

3. **SPI_DMA_TX_ENA**
   - Description:
     - Set this bit to enable DMA-controlled send data mode (R/W).

4. **SPI_RX_AFIRO_RST**
   - Description:
     - Set this bit to reset spi_rx_aiffo as shown in Figure 30.5-3 and in Figure 30.5-4.
     - spi_rx_aiffo is used to receive data in SPI master and slave transfer.

5. **SPI_BUF_AFIRO_RST**
   - Description:
     - Set this bit to reset buf_tx_aiffo as shown in Figure 30.5-3 and in Figure 30.5-4.
     - buf_tx_aiffo is used to send data out in CPU-controlled master and slave transfer.

6. **SPI_DMA_AFIRO_RST**
   - Description:
     - Set this bit to reset dma_tx_aiffo as shown in Figure 30.5-3 and in Figure 30.5-4.
     - dma_tx_aiffo is used to send data out in DMA-controlled slave transfer.

**Additional Information:**

- **SPI_DMA_OUTFIFO_EMPTY**
  - Description:
    - Records the status of DMA TX FIFO (1 = DMA TX FIFO not ready for sending data, 0 = DMA TX FIFO ready for sending data).

- **SPI_DMA_INFIFO_FULL**
  - Description:
    - Records the status of DMA RX FIFO (1 = DMA RX FIFO is not ready to receive data; 0 = DMA RX FIFO already has received data).
  
- **SPI_DMA_SLV_SEGTrans_EN**
  - Description: 
    - Enable DMA-controlled segmented transfer in slave half-duplex mode. (R/W)

- **SPI_SLV_RX_SEGTrans_CLR_EN**
  - Description:
    - In DMA-controlled half-duplex slave mode, if the size of DMA RX buffer is smaller than that received data; it will not be updated.
  
- **SPI_SLV_TX_SEGTrans_CLR_EN**
  - Description: 
    - In DMA-controlled half-duplex slave mode, if the size of DMA TX buffer (R/W) 

**Footer Information:** 
- Page number and document version:
  - "1162 ESP32-S3 TRM (Version 1.7)"
  
- Company information:
  - Espressif Systems

- Document action link: [Submit Documentation Feedback](#)