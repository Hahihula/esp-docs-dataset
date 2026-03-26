

```markdown
Master sends 0x06 CMD (En_QPI) to set GP-SPI slave to QPI mode and all the states of supported transfer will be in 4-bit mode afterwards. If 0xDD CMD (Ex_QPI) is received, GP-SPI slave will be back to SPI mode.

Other transfer types than these described in Table 43.5-16 and Table 43.5-17 are ignored. But if the CS low-level duration is longer than two APB_CLK cycles, SPI_TRANS_DONE_INT will be triggered. For more information on interrupts triggered at the end of transmissions, please refer to Section 43.11.

### 43.5.10.3 Slave Single Transfer and Slave Segmented Transfer

When GP-SPI works as a slave, it supports full-duplex and half-duplex communications controlled by DMA and by CPU. DMA-controlled transfer can be a single transfer, or a slave segmented transfer consisting of several transactions (segments). The CPU-controlled transfer can only be one single transfer, since each CPU-controlled transaction needs to be triggered by CPU.

In a slave segmented transfer, all transfer types listed in Table 43.5-16 and Table 43.5-17 are supported in a single transaction (segment). It means that CPU-controlled transaction and DMA-controlled transaction can be mixed in one slave segmented transfer.

It is recommended that in a slave segmented transfer:

*   CPU-controlled transaction is used for handshake communication and short data transfers.
*   DMA-controlled transaction is used for large data transfers.

### 43.5.10.4 Configuration of Slave Single Transfer

When operating as slave, GP-SPI supports CPU/DMA-controlled full-duplex/half-duplex single transfers.

The register configuration procedure is as follows (take GP-SPI2 as an example):

1.  Configure the IO path via HP IO MUX or HP GPIO matrix between GP-SPI2 and an external SPI device.
2.  Configure AHB clock (AHB_CLK).
3.  Set `SPI_SLAVE_MODE` to enable slave mode.
4.  Configure `SPI_DOUTDIN`:

    *   1: enable full-duplex communication.
    *   0: enable half-duplex communication.

5.  Prepare data:

    *   if CPU-controlled transfer is selected and GP-SPI2 is used to send data, then prepare data in registers `SPI_WO_REG~SPI_W15_REG`.
    *   if DMA-controlled transfer is selected,

        -   configure `SPI_DMA_TX_ENA/SPI_DMA_RX_ENA` and `SPI_RX_EOF_EN`.
        -   configure DMA TX/RX link,
        -   and start DMA TX/RX engine, as described in Section 43.5.7 and Section 43.5.8.

6.  Set `SPI_DMA_AFIFO_RST`, `SPI_BUF_AFIFO_RST`, and `SPI_RX_AFIFO_RST` to reset these buffers.
```