

```markdown
| Internal Interrupt Source                     | Trigger Condition                                                                                                                                                                                                                       | Interrupt Signal |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| SPI_DMA_SEG_TRAN_DONE_INT                    | At the end of End_SEG_TRANS transfer in GP-SPI2 slave segmented transfer mode or at the end of master configurable segmented transfer mode                                                                                                 | SPI_INTR        |
| SPI_SEG_MAGIC_ERR_INT                        | A Magic error occurs in CONF buffer during configurable segmented transfer when GP-SPI2 works as master                                                                                                                                 | SPI_INTR        |
| SPI_MST_RX_AFIFO_WFULL_ERR_INT                | RX AFIFO write-full error when GP-SPI2 works as master                                                                                                                                                    | SPI_INTR        |
| SPI_MST_TX_AFIFO_REMPTY_ERR_INT               | TX AFIFO read-empty error when GP-SPI2 works as master                                                                                                                                                      | SPI_INTR        |
| SPI_SLV_CMD_ERR_INT                           | A received command value is not supported when GP-SPI2 works as slave                                                                                                                                                | SPI_INTR        |
| SPI_APP2_INT                                  | Set SPI_APP2_INT_SET (Only used for user defined function)                                                                                                                                                              | SPI_INTR        |
| SPI_APP1_INT                                  | Set SPI_APP1_INT_SET (Only used for user defined function)                                                                                                                                                              | SPI_INTR        |

## 26.9.2 Interrupts Used in Master and in Slave

Table 26.9-2 and Table 26.9-3 show the interrupts used in GP-SPI2 master and slave modes. Set the interrupt enable bit `SPI_*_INT_ENA` in `SPI_DMA_INT_ENA_REG` and wait for the interrupt. When the transfer ends, the related interrupt is triggered and should be cleared by software before the next transfer.

Table 26.9-2. GP-SPI2 Master Mode Interrupts

| Transfer Type                     | Communication Mode       | Controlled by | Interrupt                                                                 |
|-----------------------------------|--------------------------|---------------|---------------------------------------------------------------------------|
| Single Transfer                   | Full-duplex              | DMA           | GDMA_IN_SUC_EOF_Chn_INT¹                                                |
|                                   |                          | CPU           | SPI_TRAN_DONE_INT²                                                      |
|                                   | Half-duplex MOSI Mode    | DMA           | SPI_TRAN_DONE_INT                                                       |
|                                   |                          | CPU           | SPI_TRAN_DONE_INT                                                       |
|                                   | Half-duplex MISO Mode    | DMA           | GDMA_IN_SUC_EOF_Chn_INT                                                |
|                                   |                          | CPU           | SPI_TRAN_DONE_INT                                                       |
| Configurable Segmented Transfer   | Full-duplex              | DMA           | SPI_DMA_SEG_TRANS_DONE_INT³                                            |
|                                   |                          | CPU           | Not supported                                                            |
|                                   | Half-duplex MOSI Mode    | DMA           | SPI_DMA_SEG_TRANS_DONE_INT                                              |
|                                   |                          | CPU           | Not supported                                                            |
|                                   | Half-duplex MISO         | DMA           | SPI_DMA_SEG_TRANS_DONE_INT                                              |
|                                   |                          | CPU           | Not supported                                                            |
```