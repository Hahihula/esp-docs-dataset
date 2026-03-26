

```markdown
Register 39.102. H264_DMA_IN_CONFO_CH3_REG (0x0800)

Continued from the previous page...

H264_DMA_IN_CMD_DISABLE_CH3 Configures whether to disable command on RX channel 3.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CH3 Configures whether to disable weight arbitration for RX channel 3.
O: Enable
1: Disable
(R/W)

Register 39.103. H264_DMA_IN_POP_CH3_REG (0x0818)
```

```markdown
H264_DMA_INFIFO_RDATA_CH3 Represents the data popped from DMA RX FIFO. (RO)

H264_DMA_INFIFO_POP_CH3 Configures whether to pop data from DMA RX FIFO.
O: No effect
1: Pop
(R/W/SC)
```

```text
31
+---------------------------------------------+
| (reserved)                                 |
| H264_DMA_INFIFO_POP_CH3                    |
| H264_DMA_INFIFO_RDATA_CH3                  |
+---------------------------------------------+
  0x400 Reset
```