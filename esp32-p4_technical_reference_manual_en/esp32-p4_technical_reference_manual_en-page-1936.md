

```markdown
Register 39.97. H264_DMA_IN_CONFO_CH2_REG (0x0700)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0x0| 0  | 0  | 0  | (reserved) | H264_DMA_IN_PAGE_BOUND_EN_CH2 | H264_DMA_IN_MEM_BURST_LENGTH_CH2 | H264_DMA_IN_CHECK_OWNER_CH2 | H264_DMA_IN_ECC_AES_EN_CH2 | H264_DMA_IN_RST_CH2 | (reserved) | H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH2 | H264_DMA_IN_CMD_DISABLE_CH2 | H264_DMA_IN检查位CH2 | (reserved) |
```

H264_DMA_INDSCR_BURST_EN_CH2 Configures whether to enable INCR burst transfer for RX channel 2 to read descriptors.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ECC_AES_EN_CH2 Configures whether DMA can access external memory space for ECC and AES via RX channel 2.
O: Not access
1: Access. In this case, the start address of the memory region should be 16-byte aligned. The product of the width and the bytes per pixel must also be 16-byte aligned.
(R/W)

H264_DMA_IN_CHECK_OWNER_CH2 Configures whether to enable owner bit check for RX channel 2.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_MEM_BURST_LENGTH_CH2 Configures the burst length for RX channel 2.
0: 8 bytes
1: 16 bytes
2: 32 bytes
3: 64 bytes
4: 128 bytes
5 ~ 7: Invalid
(R/W)

H264_DMA_IN_PAGE_BOUND_EN_CH2 Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length.
O: AXI read data can cross the address boundary
1: AXI read data doesn't cross the address boundary
(R/W)

H264_DMA_IN_RST_CH2 Write 1 then write 0 to reset RX channel 2. (R/W)

Continued on the next page...
```