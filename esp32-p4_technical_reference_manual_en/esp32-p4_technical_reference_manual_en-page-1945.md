

```markdown
Register 39.107. H264_DMA_IN_CONFO_CH4_REG (0x0900)

Continued from the previous page...

H264_DMA_IN_CMD_DISABLE_CH4 Configures whether to disable command on RX channel 4.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH4 Configures whether to disable weight arbitration for RX channel 4.
O: Enable
1: Disable
(R/W)

Register 39.108. H264_DMA_IN_POP_CH4_REG (0x0918)
```

```markdown
H264_DMA_INFIFO_RDATA_CH4 Represents the data popped from DMA RX FIFO. (RO)

H264_DMA_INFIFO_POP_CH4 Configures whether to pop data from DMA RX FIFO.
O: No effect
1: Pop
(R/W/SC)
```