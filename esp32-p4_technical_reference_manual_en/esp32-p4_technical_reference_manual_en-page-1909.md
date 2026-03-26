

```markdown
Register 39.66. H264_DMA_OUT_CONF0_CH1_REG (0x0100)

| Bit | Name                                      | Description                                                                 |
|-----|--------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                |                                                                             |
| 30  | H264_DMA_OUT_ARB_WEIGHT_OPT_DIS_CH1        |                                                                             |
| 29  | H264_DMA_OUT_CMD_DISABLE_CH1               |                                                                             |
| 28  | H264_DMA_OUT_RST_CH1                       |                                                                             |
| 27  | (reserved)                                |                                                                             |
| 26  | H264_DMA_OUT_PAGE_BOUND_EN_CH1             |                                                                             |
| 25  | H264_DMA_OUT_MEM_BURST_LENGTH_CH1          |                                                                             |
| 24  | (reserved)                                |                                                                             |
| 23  | H264_DMA_OUT_CHECK_OWNER_CH1               |                                                                             |
| 22  | H264_DMA_OUT_ECC_AES_EN_CH1                |                                                                             |
| 21  | H264_DMA_OUT_EOF_MODE_CH1                  |                                                                             |
| 20  | H264_DMA_OUT_AUTO_WRBACK_CH1               | Configures whether to enable automatic outlink-writeback when all the data pointed by outlink descriptor has been received. <br> O: Disable <br> 1: Enable (R/W) |
| 19  | (reserved)                                |                                                                             |
| 18  | H264_DMA_OUT_EOF_MODE_CH1                  | Configures EOF flag generation mode for TX channel 1. <br> O: EOF flag is generated when last data has been pushed into FIFO in DMA <br> 1: EOF flag is generated when last data has been popped from FIFO in DMA (R/W) |
| 17  | H264_DMA_OUTDSCR_BURST_EN_CH1              | Configures whether to enable INCR burst transfer for TX channel 1 to read descriptors. <br> O: Disable <br> 1: Enable (R/W) |
| 16  | H264_DMA_OUT_ECC_AES_EN_CH1                | Configures whether DMA can access external memory space for ECC and AES via TX channel 1. <br> O: Not access <br> 1: Access ECC/AES area. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned. (R/W) |
| 15  | H264_DMA_OUT_CHECK_OWNER_CH1               | Configures whether to enable owner bit check for TX channel 1. <br> O: Disable <br> 1: Enable (R/W) |

Continued on the next page...
```