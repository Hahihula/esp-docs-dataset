

```markdown
- If the length of configured GDMA RX buffer is shorter than that of actual data transferred, the extra data will be lost. The interrupts `SPI_INFIFO_FULL_ERR_INT` and `SPI_TRANS_DONE_INT` are triggered. But `GDMA_IN_SUC_EOF_CHn_INT` interrupt is not generated.
- If the length of configured GDMA RX buffer is longer than that of actual data transferred, the RX buffer is not fully used, and the remaining buffer is discarded. In the following transaction, a new linked buffer will be used directly.

## 28.5.7 Data Flow Control

CPU-controlled and DMA-controlled transfers are supported in GP-SPI2 both as master and as slave.
CPU-controlled transfer means that data is transferred between registers `SPI_WO_REG ~ SPI_W15_REG` and the SPI device. DMA-controlled transfer means that data is transferred between the configured GDMA TX/RX buffer and the SPI device. To select between the two transfer modes, configure `SPI_DMA_RX_ENA` and `SPI_DMA_TX_ENA` before the transfer starts.

### 28.5.7.1 GP-SPI2 Functional Blocks

Figure 28.5-2 shows the main functional blocks in GP-SPI2, including:

*   Master FSM: all the features supported in GP-SPI2 as master are controlled by this state machine together with register configuration.
*   SPI Buffer: `SPI_WO_REG ~ SPI_W15_REG`. See Figure 28.5-1. The data transferred in CPU-controlled mode is prepared in this buffer.
*   Timing Module: captures data on FSPI bus.
*   `spi_mst/slv_din_ctrl` and `spi_mst/slv_dout_ctrl`: converts the TX/RX data into bytes.
*   `spi_rx_affo`: stores the received data.
*   `buf_tx_affo`: stores the data to send.
*   `dma_tx_affo`: stores the data from GDMA.
*   `clk_spi_mst`: this clock is the module clock of GP-SPI2 and derived from PLL_CLK. It is used in GP-SPI2 as master to generate SPI_CLK signal for data transfer and for slaves.

Figure 28.5-2. GP-SPI2 Block Diagram
```