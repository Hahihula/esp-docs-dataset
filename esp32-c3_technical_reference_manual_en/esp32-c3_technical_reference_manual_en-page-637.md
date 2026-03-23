

```markdown
Chapter 27 SPI Controller (SPI)
GoBack

data is not guaranteed. But if the CS low time is longer than 2 APB clock (APB_CLK) cycles, 
SPI_TRANS_DONE_INT will be triggered. For more information on interrupts triggered at the end of transmissions, please refer to Section 27.9.

27.5.9.3 Slave Single Transfer and Slave Segmented Transfer

When GP-SPI2 works as a slave, it supports full-duplex and half-duplex communications controlled by DMA and by CPU. DMA-controlled transfer can be a single transfer, or a slave segmented transfer consisting of several transactions (segments). The CPU-controlled transfer can only be one single transfer, since each CPU-controlled transaction needs to be triggered by CPU.

In a slave segmented transfer, all transfer types listed in Table 27.5-11 and Table 27.5-12 are supported in a single transaction (segment). It means that CPU-controlled transaction and DMA-controlled transaction can be mixed in one slave segmented transfer.

It is recommended that in a slave segmented transfer:

*   CPU-controlled transaction is used for handshake communication and short data transfers.
*   DMA-controlled transaction is used for large data transfers.

27.5.9.4 Configuration of Slave Single Transfer

In slave mode, GP-SPI2 supports CPU/DMA-controlled full-duplex/half-duplex single transfers. The register configuration procedure is as follows:

1.  Configure the IO path via IO MUX or GPIO matrix between GP-SPI2 and an external SPI device.
2.  Configure APB clock (APB_CLK).
3.  Set the bit `SPI_SLAVE_MODE`, to enable slave mode.
4.  Configure `SPI_DOUTDIN`:

    *   1: enable full-duplex communication.
    *   0: enable half-duplex communication.

5.  Prepare data:

    *   if CPU-controlled transfer mode is selected and GP-SPI2 is used to send data, then prepare data in registers `SPI_WO_REG ~ SPI_W15_REG`.
    *   if DMA-controlled transfer mode is selected,

        -   configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA` and `SPI_RX_EOF_EN`.
        -   configure GDMA TX/RX link.
        -   start GDMA TX/RX engine, as described in Section 27.5.6 and Section 27.5.7.

6.  Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.

7.  Clear `SPI_DMA_SLV_SEG_TRANS_EN` in register `SPI_DMA_CONF_REG` to enable slave single transfer mode.

8.  Set `SPI_TRANS_DONE_INT_ENA` in `SPI_DMA_INT_ENA_REG` and wait for the interrupt `SPI_TRANS_DONE_INT`. In DMA-controlled mode, it is recommended to wait for the interrupt
```