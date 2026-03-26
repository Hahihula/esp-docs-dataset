

```markdown
Register 39.58. H264_DMA_OUT_CONF0_CHO_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | H264_DMA_OUT_ARB_WEIGHT_OPT_DIS_CHO | H264_DMA_OUT_CMD_DISABLE_CHO | H264_DMA_OUT_RST_CHO | (reserved) | H264_DMA_OUT_REORDER_EN_CHO | (reserved) | H264_DMA_OUT_PAGE_BOUND_EN_CHO | (reserved) | H264_DMA_OUT_MEM_BURST_LENGTH_CHO | (reserved) | H264_DMA_OUT_CHECK_OWNER_CHO | H264_DMA_OUT_OFSR_EN_CHO | H264_DMA_OUT_EOF_MODE_CHO | H264_DMA_OUT_AUTO_WRBACK_CHO |
|     | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0 | 0 | 0 | 0 | 1 | 0 | Reset |

H264_DMA_OUT_AUTO_WRBACK_CHO Configures whether to enable automatic outlink-writeback when all the data pointed by outlink descriptor has been received.
- O: Disable
- 1: Enable
(R/W)

H264_DMA_OUT_EOF_MODE_CHO Configures EOF flag generation mode for TX channel 0.
- O: EOF flag is generated when last data has been pushed into FIFO in DMA
- 1: EOF flag is generated when last data has been popped from FIFO in DMA
(R/W)

H264_DMA_OUTDSCR_BURST_EN_CHO Configures whether to enable INCR burst transfer for TX channel 0 to read descriptors.
- O: Disable
- 1: Enable
(R/W)

H264_DMA_OUT_ECC_AES_EN_CHO Configures whether DMA can access external memory space for ECC and AES via TX channel 0.
- O: Disable access
- 1: Enable access to the ECC/AES area. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.
(R/W)

H264_DMA_OUT_CHECK_OWNER_CHO Configures whether to enable owner bit check for TX channel 0.
- O: Disable
- 1: Enable
(R/W)
```