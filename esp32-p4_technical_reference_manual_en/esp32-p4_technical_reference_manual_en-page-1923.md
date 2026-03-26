

```markdown
Register 39.81. H264_DMA_OUT_CONF0_CH4_REG (0x0400)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | H264_DMA_OUT_ARB_WEIGHT_OPT_DIS_CH4 | (reserved) | H264_DMA_OUT_PAGE_BOUND_EN_CH4 | (reserved) | H264_DMA_OUT_MEM_BURST_LENGTH_CH4 | H264_DMA_OUT_CHECK_OWNER_CH4 | H264_DMA_OUT_ECC_AES_EN_CH4 | H264_DMA_OUT_OUTSCR_BURST_EN_CH4 | H264_DMA_OUT_EOF_MODE_CH4 | H264_DMA_OUT_AUTO_WRBACK_CH4 | Reset |
| Value | 0x0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 |

H264_DMA_OUT_AUTO_WRBACK_CH4 Configures whether to enable automatic outlink-writeback when all the data pointed by outlink descriptor has been received.
- O: Disable
- 1: Enable
(R/W)

H264_DMA_OUT_EOF_MODE_CH4 Configures EOF flag generation mode for TX channel 4.
- O: EOF flag is generated when last data has been pushed into FIFO in DMA
- 1: EOF flag is generated when last data has been popped from FIFO in DMA
(R/W)

H264_DMA_OUTDSCR_BURST_EN_CH4 Configures whether to enable INCR burst transfer for TX channel 4 to read descriptors.
- O: Disable
- 1: Enable
(R/W)

H264_DMA_OUT_ECC_AES_EN_CH4 Configures whether DMA can access external memory space for ECC and AES via TX channel 4.
- O: Not access
- 1: Access ECC/AES area. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.
(R/W)

H264_DMA_OUT_CHECK_OWNER_CH4 Configures whether to enable owner bit check for TX channel 4.
- O: Disable
- 1: Enable
(R/W)
```