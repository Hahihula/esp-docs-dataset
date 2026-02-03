**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Navigation Link:**
GoBack

**Body Text with Code Blocks and Lists:**

In slave mode, if GDMA_IN_SUC_EOF_CHn_INTENA is set, then the interrupt GDMA_IN_SUC_EOF_CHn_INT will be triggered when one of conditions listed in Table 30.5-7 are met.

**Table Title:**
Table 30.5-7. Interrupt Trigger Condition on GP-SPI Data Transferer in Slave Mode

| Transfer Type | Control Bit^1 | Control Bit^2 | Condition |
|---------------|---------------|---------------|-----------|
| Slave Single Transfer | O | O | A single transfer is done. |
| | 1 | 0 | A single transfer is done. Or the length of the received data is equal to (SPI_MS_DATA_BITLEN + 1) |
| Slave Segmented Transfer | O | 1 | (CMD7 or End_SEGTrans) is received correctly. |
| | 1 | 1 | (CMD7 or End_SEGTrans) is received correctly. Or the length of the received data is equal to (SPI_MS_DATA_BITLEN + 1) |

**Subsection Title:**
30.5.6.2 GDMA TX/RX Buffer Length Control

It is recommended that the length of configured GDMA TX/RX buffer is equal to the length of real transferred data.

- If the length of configured GDMA TX buffer is shorter than that of real transferred data, the extra data will be the same as the last transferred data. SPI_OUTFIFO_EMPTY_ERR_INT and GDMA_OUT_EOF_CHn_INT are triggered.
- If the length of configured GDMA TX buffer is longer than that of real transferred data, the TX buffer is not fully used, and the remaining buffer is available for following transaction even if a new TX buffer is linked later. Please keep it in mind. Or save the unused data and reset DMA.

- If the length of configured GDMA RX buffer is shorter than that of real transferred data, the extra data will be lost. The interrupts SPI_INFIFO_FULL_ERR_INT and SPITransDONE_INT are triggered. But GDMA_IN_SUC_EOF_CHn_INT interrupt is not generated.
  - If the length of configured GDMA RX buffer is longer than that of real transferred data, the RX buffer is not fully used, and the remaining buffer is discarded. In the following transaction, a new linked buffer will be used directly.

**Subsection Title:**
30.5.7 Data Flow Control in GP-SPI Master and Slave Modes

CPU-controlled and DMA-controlled transfers are supported in GP-SPI master and slave modes.
- CPU-controlled transfer means that data transfers between registers SPI_WO_REG ~ SPI_W15_REG and the SPI device. DMA-controlled transfer means that data transfers between the configured GDMA TX/RX buffer and the SPI device.

To select between the two transfer modes, configure SPI_DMA_RX_ENA and SPI_DMA_TX_ENA before the transfer starts.

**Footer:**
Espressif Systems
Submit Documentation Feedback

ESP32-S3 TRM (Version 1.7)