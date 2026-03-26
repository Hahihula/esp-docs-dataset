

```markdown
7. Clear SPI_DMA_SLV_SEG_TRANS_EN in register SPI_DMA_CONF_REG to enable slave single transfer.
8. Set SPI_TRANS_DONE_INT_ENA in register SPI_DMA_INT_ENA_REG and wait for the interrupt SPI_TRANS_DONE_INT. In DMA-controlled mode, it is recommended to wait for the interrupt AXI_DMA_IN_SUC_EOF_CHn_INT when DMA RX buffer is used, which means that data has been stored in the related memory. Other interrupts described in Section 43.11 are optional.

## 43.5.10.5 Configuration of Slave Segmented Transfer in Half-Duplex

DMA must be used in this mode. The register configuration procedure is as follows (take GP-SPI2 as an example):

1. Configure the IO path via HP IO MUX or HP GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure APB clock (APB_CLK).
3. Set SPI_SLAVE_MODE to enable slave mode.
4. Clear SPI_DOUTDIN to enable half-duplex communication.
5. Prepare data in registers SPI_W0_REG~SPI_W15_REG, if needed.
6. Set SPI_DMA_AFIFO_RST, SPI_BUF_AFIFO_RST, and SPI_RX_AFIFO_RST to reset these buffers.
7. Set bits SPI_DMA_RX_ENA and SPI_DMA_TX_ENA. Clear the bit SPI_RX_EOF_EN. Configure DMA TX/RX link and start DMA TX/RX engine, as shown in Section 43.5.7 and Section 43.5.8.
8. Set SPI_DMA_SLV_SEG_TRANS_EN in register SPI_DMA_CONF_REG to enable slave segmented transfer.
9. Set SPI_SEG_TRANS_DONE_INT_ENA in register SPI_DMA_INT_ENA_REG and wait for the interrupt SPI_DMA_SEG_TRANS_DONE_INT, which means that the segmented transfer has finished and data has been put into the related memory. Other interrupts described in Section 43.11 are optional.

When End_SEG_TRANS (0x05 in SPI mode, 0xA5 in QPI mode) is received by GP-SPI, this slave segmented transfer is ended and the interrupt SPI_DMA_SEG_TRANS_DONE_INT is triggered.

## 43.5.10.6 Configuration of Slave Segmented Transfer in Full-Duplex

DMA must be used in this mode. In such transfer, the data is transferred from and to the DMA buffer. The interrupt AXI_DMA_IN_SUC_EOF_CHn_INT is triggered when the transfer ends.

The register configuration procedure is as follows (take GP-SPI2 as an example):

1. Configure the IO path via HP IO MUX or HP GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure APB clock (APB_CLK).
3. Set SPI_SLAVE_MODE and SPI_DOUTDIN, to enable slave full-duplex communication.
4. Set SPI_DMA_AFIFO_RST, SPI_BUF_AFIFO_RST, and SPI_RX_AFIFO_RST to reset these buffers.
5. Set SPI_DMA_TX_ENA/SPI_DMA_RX_ENA. Configure DMA TX/RX link and start DMA TX/RX engine, as shown in Section 43.5.7 and Section 43.5.8.
6. Set SPI_RX_EOF_EN in register SPI_DMA_CONF_REG. Configure SPI_MS_DATA_BITLEN[17:0] in register SPI_MS_DLEN_REG to the bit length of the received DMA data.
7. Set SPI_DMA_SLV_SEG_TRANS_EN in register SPI_DMA_CONF_REG to enable slave segmented transfer.
```