

```markdown
Register 39.97. H264_DMA_IN_CONF0_CH2_REG (0x0700)

Continued from the previous page...

H264_DMA_IN_CMD_DISABLE_CH2 Configures whether to disable command on RX channel 2.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH2 Configures whether to disable weight arbitration for
RX channel 2.
O: Enable
1: Disable
(R/W)

Register 39.98. H264_DMA_IN_POP_CH2_REG (0x0718)


H264_DMA_INFIFO_RDATA_CH2 Represents the data popped from DMA RX FIFO. (RO)

H264_DMA_INFIFO_POP_CH2 Configures whether to pop data from DMA RX FIFO.
O: No effect
1: Pop
(R/W/SC)
```