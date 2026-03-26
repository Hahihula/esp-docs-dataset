

```markdown
Register 39.67. H264_DMA_OUT_PUSH_CH1_REG (0x0118)

| Bit | Description                  |
|-----|------------------------------|
| 31  | (reserved)                   |
| 11  |                              |
| 10  |                              |
| 9   |                              |
| 0   | H264_DMA_OUTFIFO_PUSH_CH1    |
|     |                              |
|     | Ox0                          |
|     | Reset                        |

H264_DMA_OUTFIFO_WDATA_CH1 Represents the data that needs to be pushed into DMA TX FIFO.
(R/W)

H264_DMA_OUTFIFO_PUSH_CH1 Configures whether to push data into DMA TX FIFO.
0: No effect
1: Push
(R/W/SC)
```