

```markdown
Register 39.71. H264_DMA_OUT_CONFO_CH2_REG (0x0200)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | H264_DMA_OUT_ARB_WEIGHT_OPT_DS_CH2         |                                                                             |
| 29  | H264_DMA_OUT_ARB_CMD_DISABLE_CH2           |                                                                             |
| 28  | H264_DMA_OUT_RST_CH2                       |                                                                             |
| 27  | (reserved)                                 |                                                                             |
| 26  | H264_DMA_OUT_PAGE_BOUND_EN_CH2             |                                                                             |
| 25  | H264_DMA_OUT_MEM_BURST_LENGTH_CH2          |                                                                             |
| 24  | (reserved)                                 |                                                                             |
| 23  | H264_DMA_OUT_CHECK_OWNER_CH2               |                                                                             |
| 22  | H264_DMA_OUT_ECC_AES_EN_CH2                |                                                                             |
| 21  | H264_DMA_OUT_EOF_MODE_CH2                  |                                                                             |
| 20  | (reserved)                                 |                                                                             |
| 19  | H264_DMA_OUT_AUTO_WRBACK_CH2               | Configures whether to enable automatic outlink-writeback when all the data pointed by outlink descriptor has been received. O: Disable<br>1: Enable<br>(R/W) |
| 18  | (reserved)                                 |                                                                             |
| 17  | H264_DMA_OUT_OUTSCR_BURST_EN_CH2           | Configures whether to enable INCR burst transfer for TX channel 2 to read descriptors. O: Disable<br>1: Enable<br>(R/W) |
| 16  | (reserved)                                 |                                                                             |
| 15  | H264_DMA_OUTDSCR_BURST_EN_CH2              | Configures whether DMA can access external memory space for ECC and AES via TX channel 2. O: Not access<br>1: Access ECC/AES area. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.<br>(R/W) |
| 14  | (reserved)                                 |                                                                             |
| 13  | H264_DMA_OUT_CHECK_OWNER_CH2               | Configures whether to enable owner bit check for TX channel 2. O: Disable<br>1: Enable<br>(R/W) |

Continued on the next page...
```