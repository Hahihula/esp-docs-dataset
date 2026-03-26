

```markdown
Register 39.71. H264_DMA_OUT_CONFO_CH2_REG (0x0200)

Continued from the previous page...

H264_DMA_OUT_MEM_BURST_LENGTH_CH2 Configures the burst length for TX channel 2.
0: 8 bytes
1: 16 bytes
2: 32 bytes
3: 64 bytes
4: 128 bytes
5 ~ 7: Invalid
(R/W)

H264_DMA_OUT_PAGE_BOUND_EN_CH2 Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length.
0: AXI read data can cross the address boundary
1: AXI read data doesn't cross the address boundary
(R/W)

H264_DMA_OUT_RST_CH2 Write 1 then write 0 to reset TX channel 2. (R/W)

H264_DMA_OUT_CMD_DISABLED_CH2 Configures whether to disable command on TX channel 2.
0: Disable
1: Enable
(R/W)

H264_DMA_OUT_ARB_WEIGHT_OPT_DIS_CH2 Configures whether to disable weight arbitration for TX channel 2.
0: Enable
1: Disable
(R/W)
```