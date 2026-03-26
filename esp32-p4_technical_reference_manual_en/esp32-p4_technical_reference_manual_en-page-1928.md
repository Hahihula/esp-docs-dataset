

```markdown
Chapter 39 H264 Encoder

Register 39.86. H264_DMA_IN_CONFO_CHO_REG (0x0500)

Continued from the previous page...

H264_DMA_IN_CMD_DISABLE_CHO Configures whether to disable command on RX channel 0.
O: Disable
1: Enable
(R/W)

H264_DMA_IN_ARB_WEIGHT_OPT_DIS_CHO Configures whether to disable weight arbitration for
RX channel 0.
O: Enable
1: Disable
(R/W)

Register 39.87. H264_DMA_IN_POP_CHO_REG (0x0518)
```

```markdown
| Bit Range | Field Name                     | Description                                                                 |
|-----------|---------------------------------|-----------------------------------------------------------------------------|
| 31        |                                | (reserved)                                                                  |
|           |                                |                                                                             |
|           | H264_DMA_INFIFO_POP_CHO         |                                                                             |
|           | H264_DMA_INFIFO_RDATA_CHO       |                                                                             |
| 12..10    |                                 | 0x400                                                                       |
| 9..0      |                                 | Reset                                                                       |

H264_DMA_INFIFO_RDATA_CHO Represents the data popped from DMA RX FIFO. (RO)

H264_DMA_INFIFO_POP_CHO Configures whether to pop data from DMA RX FIFO.
O: No effect
1: Pop
(R/W/SC)
```