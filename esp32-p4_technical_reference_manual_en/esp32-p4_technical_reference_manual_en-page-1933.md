

```markdown
Chapter 39 H264 Encoder

Register 39.92. H264_DMA_IN_CONFO_CH1_REG (0x0600)

Continued from the previous page...

H264_DMA_IN_CMD_DISABLE_CH1 Configures whether to disable command on RX channel 1.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH1 Configures whether to disable weight arbitration for RX channel 1.
O: Enable
1: Disable
(R/W)

Register 39.93. H264_DMA_IN_POP_CH1_REG (0x0618)

H264_DMA_INFIFO_RDATA_CH1 Represents the data popped from DMA RX FIFO. (RO)

H264_DMA_INFIFO_POP_CH1 Configures whether to pop data from DMA RX FIFO.
O: No effect
1: Pop
(R/W/SC)
```