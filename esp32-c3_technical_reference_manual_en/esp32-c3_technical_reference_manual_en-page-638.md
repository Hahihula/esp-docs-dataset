

```markdown
GDMA_IN_SUC_EOF_CHn_INT when GDMA RX buffer is used, which means that data has been stored in the related memory. Other interrupts described in Section 27.9 are optional.

### 27.5.9.5 Configuration of Slave Segmented Transfer in Half-Duplex

GDMA must be used in this mode. The register configuration procedure is as follows:

1. Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure APB clock (APB_CLK).
3. Set `SPI_SLAVE_MODE` to enable slave mode.
4. Clear `SPI_DOUTDIN` to enable half-duplex communication.
5. Prepare data in registers `SPI_W0_REG ~ SPI_W15_REG`, if needed.
6. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST` and `SPI_RX_AFIFO_RST` to reset these buffers.
7. Set bits `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA`. Clear the bit `SPI_RX_EOF_EN`. Configure GDMA TX/RX link and start GDMA TX/RX engine, as shown in Section 27.5.6 and Section 27.5.7.
8. Set `SPI_DMA_SLV_SEG_TRANS_EN` in `SPI_DMA_CONF_REG` to enable slave segmented transfer.
9. Set `SPI_DMA_SEG_TRANS_DONE_INT_EN` in `SPI_DMA_INT_ENA_REG` and wait for the interrupt `SPI_DMA_SEG_TRANS_DONE_INT`, which means that the segmented transfer has finished and data has been put into the related memory. Other interrupts described in Section 27.9 are optional.

When End_SEG_TRANS (0x05 in SPI mode, 0xA5 in QPI mode) is received by GP-SPI2, this slave segmented transfer is ended and the interrupt `SPI_DMA_SEG_TRANS_DONE_INT` is triggered.

### 27.5.9.6 Configuration of Slave Segmented Transfer in Full-Duplex

GDMA must be used in this mode. In such transfer, the data is transferred from and to the GDMA buffer. The interrupt `GDMA_IN_SUC_EOF_CHn` _INT is triggered when the transfer ends. The configuration procedure is as follows:

1. Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure APB clock (APB_CLK).
3. Set `SPI_SLAVE_MODE` and `SPI_DOUTDIN` to enable full-duplex communication in slave mode.
4. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` bit, to reset these buffers.
5. Set `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA`. Configure GDMA TX/RX link and start GDMA TX/RX engine, as shown in Section 27.5.6 and Section 27.5.7.
6. Set the bit `SPI_RX_EOF_EN` in register `SPI_DMA_CONF_REG`. Configure `SPI_MS_DATA_BITLEN[17:0]` in register `SPI_MS_DLEN_REG` to the byte length of the received DMA data.
7. Set `SPI_DMA_SLV_SEG_TRANS_EN` in `SPI_DMA_CONF_REG` to enable slave segmented transfer mode.
8. Set `GDMA_IN_SUC_EOF_CHn_INT_ENA` and wait for the interrupt `GDMA_IN_SUC_EOF_CHn_INT`.
```