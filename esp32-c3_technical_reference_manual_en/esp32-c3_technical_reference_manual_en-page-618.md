

```markdown
End_SEG_TRAN) is received correctly or the length of GDMA RX received data is equal to (SPI_MS_DATA_BITLEN + 1).

### 27.5.6.2 GDMA TX/RX Buffer Length Control

It is recommended that the length of configured GDMA TX/RX buffer is equal to the length of real transferred data.

*   If the length of configured GDMA TX buffer is shorter than that of real transferred data, the extra data will be the same as the last transferred data. `SPI_OUTFIFO_EMPTY_ERR_INT` and `GDMA_OUT_EOF_CHn_INT` are triggered.
*   If the length of configured GDMA TX buffer is longer than the that of real transferred data, the TX buffer is not fully used, and the remaining buffer is available for following transaction even if a new TX buffer is linked later. Please keep it in mind. Or save the unused data and reset DMA.
*   If the length of configured GDMA RX buffer is shorter than that of real transferred data, the extra data will be lost. The interrupts `SPI_INFIFO_FULL_ERR_INT` and `SPI_TRANS_DONE_INT` are triggered. But `GDMA_IN_SUC_EOF_CHn_INT` interrupt is not generated.
*   If the length of configured GDMA RX buffer is longer than that of real transferred data, the RX buffer is not fully used, and the remaining buffer is discarded. In the following transaction, a new linked buffer will be used directly.

### 27.5.7 Data Flow Control in GP-SPI2 Master and Slave Modes

CPU-controlled and DMA-controlled transfers are supported in GP-SPI2 master and slave modes.
CPU-controlled transfer means that data transfers between registers `SPI_W0_REG ~ SPI_W15_REG` and the SPI device. DMA-controlled transfer means that data transfers between the configured GDMA TX/RX buffer and the SPI device. To select between the two transfer modes, configure `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA` before the transfer starts.

#### 27.5.7.1 GP-SPI2 Functional Blocks

Figure 27.5-2 shows main functional blocks in GP-SPI2, including:
```