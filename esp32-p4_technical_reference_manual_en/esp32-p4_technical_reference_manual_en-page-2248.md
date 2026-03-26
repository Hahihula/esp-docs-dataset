

```markdown
| Internal Interrupt Source | Trigger Condition                                                                 | Interrupt Signal |
|----------------------------|------------------------------------------------------------------------------------|------------------|
| LP_SPI_WAKEUP_INT          | Pre-defined chars are received and wake_up signal is generated                    | LP_SPI_INTR      |

LP-SPI is a simplified version of GP-SPI, which contains only some GP-SPI interrupt sources. Each interrupt source has a common set of configuration registers, see the Interrupt Registers in Section Register Summary.

## 43.11.2 Interrupts Used in Master and in Slave (Take GP-SPI as an Example)

Table 43.11-2 and Table 43.11-3 show the interrupts used in GP-SPI master and slave modes. Set the interrupt enable bit SPI_*_INT_ENA in SPI_DMA_INT_ENA_REG and wait for the interrupt. When the transfer ends, the related interrupt is triggered and should be cleared by software before the next transfer.

Table 43.11-2. GP-SPI Master Mode Interrupts

| Transfer Type             | Communication Mode         | Controlled by | Interrupt                                                                 |
|----------------------------|-----------------------------|---------------|---------------------------------------------------------------------------|
| Single Transfer           |                             |               |                                                                           |
|                            | Full-duplex                 | DMA           | AXI_DMA_IN_SUC_EOF_CHn_INT¹                                            |
|                            |                            | CPU           | SPI_TRANS_DONE_INT²                                                     |
|                            | Half-duplex MOSI Mode       | DMA           | SPI_TRANS_DONE_INT                                                      |
|                            |                            | CPU           | SPI_TRANS_DONE_INT                                                      |
|                            | Half-duplex MISO Mode       | DMA           | AXI_DMA_IN_SUC_EOF_CHn_INT¹                                            |
|                            |                            | CPU           | SPI_TRANS_DONE_INT                                                      |
| Configurable Segmented Transfer | Full-duplex                 | DMA           | SPI_DMA_SEG_TRANS_DONE_INT³                                           |
|                            |                             | CPU           | Not supported                                                             |
|                            | Half-duplex MOSI Mode       | DMA           | SPI_DMA_SEG_TRANS_DONE_INT                                              |
|                            |                             | CPU           | Not supported                                                             |
|                            | Half-duplex MISO            | DMA           | SPI_DMA_SEG_TRANS_DONE_INT                                              |
|                            |                             | CPU           | Not supported                                                             |

¹ If AXI_DMA_IN_SUC_EOF_Ch_n_INT is triggered, it means all the RX data of GP-SPI has been stored in the RX buffer, and the TX data has been transferred to the slave.
² SPI_TRANS_DONE_INT is triggered when CS is high, which indicates that master has completed the data exchange in SPI_WO_REG~SPI_W15_REG with slave in this mode.
³ If SPI_DMA_SEG_TRANS_DONE_INT is triggered, it means that the whole configurable segmented transfer (consisting of several segments) has finished, i.e., the RX data has been stored in the RX buffer completely and all the TX data has been sent out.
```