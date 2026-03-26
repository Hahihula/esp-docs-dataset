

```markdown
Register 39.58. H264_DMA_OUT_CONFO_CHO_REG (0x0000)

Continued from the previous page...

H264_DMA_OUT_MEM_BURST_LENGTH_CHO Configures the burst length for TX channel O.
0: 8 bytes
1: 16 bytes
2: 32 bytes
3: 64 bytes
4: 128 bytes
5 ~ 7: Invalid
(R/W)

H264_DMA_OUT_PAGE_BOUND_EN_CHO Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length.
0: AXI read data can cross the address boundary
1: AXI read data doesn't cross the address boundary
(R/W)

H264_DMA_OUT_REORDER_EN_CHO Configures whether to enable TX channel O macro block reorder.
0: Disable
1: Enable
(R/W)

H264_DMA_OUT_RST_CHO Write 1 then write 0 to reset TX channel O. (R/W)

H264_DMA_OUT_CMD_DISABLE_CHO Configures whether to disable command on TX channel O.
0: Disable
1: Enable
(R/W)

H264_DMA_OUT_ARB_WEIGHT_OPT_DIS_CHO Configures whether to disable weight arbitration for TX channel O.
0: Enable
1: Disable
(R/W)
```