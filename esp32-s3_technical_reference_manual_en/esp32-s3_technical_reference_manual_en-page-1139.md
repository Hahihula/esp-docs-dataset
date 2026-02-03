**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Body Text:**

Other transfer types than described in Table 30.5-14 and Table 30.5-15 are ignored. If the transferred data is not in unit of byte, GP-SPI can send or receive these extra bits (total bits mod 8), however, the correctness of the data is not guaranteed. But if the CS low time is longer than two APB clock (APB_CLK) cycles, SPITransDoneInt will be triggered. For more information on interrupts triggered at the end of transmissions, please refer to Section 30.10.

**Subtitle:**
30.5.9.3 Slave Single Transfer and Slave Segmented Transfer

**Body Text:**

When GP-SPI works as a slave, it supports full-duplex and half-duplex communications controlled by DMA and by CPU. DMA-controlled transfer can be a single transfer, or a slave segmented transfer consisting of several transactions (segments). The CPU-controlled transfer can only be one single transfer, since each CPU-controlled transaction needs to be triggered by CPU.

In a slave segmented transfer, all transfer types listed in Table 30.5-14 and Table 30.5-15 are supported in a single transaction (segment). It means that CPU-controlled transaction and DMA-controlled transaction can be mixed in one slave segmented transfer.

It is recommended that in a slave segmented transfer:
- CPU-controlled transaction is used for handshake communication and short data transfers.
- DMA-controlled transaction is used for large data transfers.

**Subtitle:**
30.5.9.4 Configuration of Slave Single Transfer

**Body Text:**

In slave mode, GP-SPI supports CPU/DMA-controlled full-duplex/half-duplex single transfers. The register configuration procedure is as follows:

1. Configure the IO path via IOMUX or GPIO matrix between GP-SPI and an external SPI device.
2. Configure APB clock (APB_CLK).
3. Set the bit SPI_Slave_Mode, to enable slave mode.
4. Configure SPI_DoutDin:
   - 1: enable full-duplex communication.
   - 0: enable half-duplex communication.

5. Prepare data:

   if CPU-controlled transfer mode is selected and GP-SPI is used to send data, then prepare data in registers SPI_WO_REG ~ SPI_WI5_REG.

   if DMA-controlled transfer mode is selected,

      - configure SPI_DMA_TX_ENA/SPI_DMA_RX_ENA and SPI_RX_EOF_EN.
      - configure GDMA TX/RX link.
      - start GDMA TX/RX engine, as described in Section 30.5.6 and Section 30.5.7.

6. Set SPI_DMA_AFIRO_RST, SPIBuf_Afiro_Rst, and SPI_RX_Afiro_RST to reset these buffers.

7. Clear SPI_DMA_SLV_SEG_TRANS_EN in register SPI_DMA_CONF_REG to enable slave single transfer mode.

**Footer:**
Espressif Systems
1139 Submit Documentation Feedback ESP32-S3 TRM (Version 1.7)