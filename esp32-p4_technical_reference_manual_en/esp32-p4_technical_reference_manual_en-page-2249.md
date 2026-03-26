

```markdown
| Transfer Type | Communication Mode | Controlled by | Interrupt |
|---------------|---------------------|---------------|-----------|
| Single Transfer | Full-duplex | DMA | AXI_DMA_IN_SUC_EOF_CHn_INT¹ |
|               |                     | CPU | SPI_TRANS_DONE_INT² |
|               | Half-duplex MOSI Mode | DMA (Wr_DMA) | AXI_DMA_IN_SUC_EOF_CHn_INT³ |
|               |                     | CPU (Wr_BUF) | SPI_TRANS_DONE_INT⁴ |
|               | Half-duplex MISO Mode | DMA (Rd_DMA) | SPI_TRANS_DONE_INT⁵ |
|               |                     | CPU (Rd_BUF) | SPI_TRANS_DONE_INT⁶ |
| Slave Segmented Transfer | Full-duplex | DMA | AXI_DMA_IN_SUC_EOF_CHn_INT⁷ |
|                         |             | CPU | Not supported⁸ |
|                         | Half-duplex MOSI Mode | DMA (Wr_DMA) | SPI_DMA_SEG_TRANS_DONE_INT⁹ |
|                         |                     | CPU (Wr_BUF) | Not supported¹⁰ |
|                         | Half-duplex MISO Mode | DMA (Rd_DMA) | SPI_DMA_SEG_TRANS_DONE_INT¹¹ |
|                         |                     | CPU (Rd_BUF) | Not supported¹² |

---

43.12 Register Summary

43.12.1 GP-SPI2 Register Summary

The addresses in this section are relative to GP-SPI2 base address provided in Table 7.3-2 in Chapter 7 System and Memory.

The abbreviations given in Column Access are explained in Section Access Types for Registers.
```