

```markdown
9. Set SPI_DMA_SEG_TRANS_DONE_INT_ENA in register SPI_DMA_INT_ENA_REG and wait for the interrupt SPI_DMA_SEG_TRANS_DONE_INT, which means that the segmented transfer has finished and data has been put into the related memory. Other interrupts described in Section 33.9 are optional.

When End_SEG_TRANS (0x05 in SPI mode, 0xA5 in QPI mode) is received by GP-SPI2, this slave segmented transfer is ended and the interrupt SPI_DMA_SEG_TRANS_DONE_INT is triggered.

### 33.5.10.6 Configuration of Slave Segmented Transfer in Full-Duplex

GDMA must be used in this mode. In such transfer, the data is transferred from and to the GDMA buffer. The interrupt AHB_DMA_IN_SUC_EOF_ChN_INT is triggered when the transfer ends.

The register configuration procedure is as follows:

1. Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure AHB_CLK and APB_CLK.
3. Set SPI_SLAVE_MODE and SPI_DOUTDIN, to enable slave full-duplex communication.
4. Set SPI_DMA_AFIFO_RST, SPI_BUF_AFIFO_RST, and SPI_RX_AFIFO_RST to reset these buffers.
5. Set SPI_DMA_TX_ENA and SPI_DMA_RX_ENA. Configure GDMA TX/RX link and start GDMA TX/RX engine, as shown in Section 33.5.7 and Section 33.5.8.
6. Set SPI_RX_EOF_EN in register SPI_DMA_CONF_REG. Configure SPI_MS_DATA_BITLEN[17:0] in register SPI_MS_DLEN_REG to the bit length of the received GDMA data in unit of byte.
7. Set SPI_DMA_SLV_SEG_TRANS_EN in register SPI_DMA_CONF_REG to enable slave segmented transfer.
8. Set AHB_DMA_IN_SUC_EOF_ChN_INT_ENA and wait for the interrupt AHB_DMA_IN_SUC_EOF_ChN_INT.

## 33.6 CS Setup Time and Hold Time Control

SPI bus CS (SPI_CS) setup time and hold time are very important to meet the timing requirements of various SPI devices (e.g., flash or PSRAM).

CS setup time is the time between the CS falling edge and the first latch edge of SPI bus CLK (SPI_CLK). The first latch edge for mode 0 and mode 3 is rising edge, and falling edge for mode 1 and mode 2.

CS hold time is the time between the last latch edge of SPI_CLK and the CS rising edge.

When operating as slave, the CS setup time and hold time should be longer than 0.5 x T_SPI_CLK, otherwise the SPI transfer may be incorrect. T_SPI_CLK is one cycle of SPI_CLK.

When operating as master, set the CS setup time by specifying SPI_CS_SETUP in register SPI_USER_REG and SPI_CS_SETUP_TIME in register SPI_USER1_REG.

* If SPI_CS_SETUP is cleared, the SPI CS setup time is 0.5 x T_SPI_CLK.
* If SPI_CS_SETUP is set, the SPI CS setup time is (SPI_CS_SETUP_TIME + 1.5) x T_SPI_CLK.

Set the CS hold time by specifying SPI_CS_HOLD in register SPI_USER_REG and SPI_CS_HOLD_TIME in register SPI_USER1_REG.

* If SPI_CS_HOLD is cleared, the SPI CS hold time is 0.5 x T_SPI_CLK.
```