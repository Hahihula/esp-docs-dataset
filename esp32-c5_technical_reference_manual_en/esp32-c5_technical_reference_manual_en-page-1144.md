

```markdown
33.5.10.4 Configuration of Slave Single Transfer

When operating as slave, GP-SPI2 supports CPU/DMA-controlled full-duplex/half-duplex single transfers.

The register configuration procedure is as follows:

1. Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure AHB_CLK and APB_CLK.
3. Set `SPI_SLAVE_MODE` to enable slave mode.
4. Configure `SPI_DOUTDIN`:
    - 1: enable full-duplex communication.
    - 0: enable half-duplex communication.

5. Prepare data:
    - if CPU-controlled transfer is selected and GP-SPI2 is used to send data, then prepare data in registers `SPI_WO_REG~SPI_W15_REG`.
    - if DMA-controlled transfer is selected,
        - configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA` and `SPI_RX_EOF_EN`.
        - configure GDMA TX/RX link,
            - and start GDMA TX/RX engine, as described in Section 33.5.7 and Section 33.5.8.

6. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.

7. Clear `SPI_DMA_SLV_SEG_TRANS_EN` in register `SPI_DMA_CONF_REG` to enable slave single transfer.

8. Set `SPI_TRANS_DONE_INT_ENA` in register `SPI_DMA_INT_ENA_REG` and wait for the interrupt `SPI_TRANS_DONE_INT`. In DMA-controlled mode, it is recommended to wait for the interrupt `AHB_DMA_IN_SUC_EOF_ChN_INT` when DMA RX buffer is used, which means that data has been stored in the related memory. Other interrupts described in Section 33.9 are optional.

33.5.10.5 Configuration of Slave Segmented Transfer in Half-Duplex

GDMA must be used in this mode. The register configuration procedure is as follows:

1. Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2. Configure AHB_CLK and APB_CLK.
3. Set `SPI_SLAVE_MODE` to enable slave mode.
4. Clear `SPI_DOUTDIN` to enable half-duplex communication.
5. Prepare data in registers `SPI_WO_REG~SPI_W15_REG`, if needed.

6. Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.

7. Set bits `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA`. Clear the bit `SPI_RX_EOF_EN`. Configure GDMA TX/RX link and start GDMA TX/RX engine, as shown in Section 33.5.7 and Section 33.5.8.

8. Set `SPI_DMA_SLV_SEG_TRANS_EN` in register `SPI_DMA_CONF_REG` to enable slave segmented transfer.
```