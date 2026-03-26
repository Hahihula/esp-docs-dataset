

```markdown
Register 39.59. H264_DMA_OUT_PUSH_CHO_REG (0x0018)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 11  |                              |
| 10  |                              |
| 9   |                              |
| 0   | H264_DMA_OUTFIFO_PUSH_CHO    |
|     |                              |
|     | H264_DMA_OUTFIFO_WDATA_CHO   |

H264_DMA_OUTFIFO_WDATA_CHO Represents the data that needs to be pushed into DMA TX FIFO. (R/W)

H264_DMA_OUTFIFO_PUSH_CHO Configures whether to push data into DMA TX FIFO.
0: No effect
1: Push
(R/W/SC)
```