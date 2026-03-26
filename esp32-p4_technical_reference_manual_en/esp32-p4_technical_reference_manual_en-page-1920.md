

```markdown
Register 39.76. H264_DMA_OUT_CONFO_CH3_REG (0x0300)

Continued from the previous page...

H264_DMA_OUT_MEM_BURST_LENGTH_CH3 Configures the burst length for TX channel 3.
- 0: 8 bytes
- 1: 16 bytes
- 2: 32 bytes
- 3: 64 bytes
- 4: 128 bytes
- 5 ~ 7: Invalid (R/W)

H264_DMA_OUT_PAGE_BOUND_EN_CH3 Configures whether to make sure AXI read data doesn't cross the address boundary which define by mem_burst_length.
- 0: AXI read data can cross the address boundary
- 1: AXI read data doesn't cross the address boundary (R/W)

H264_DMA_OUT_ARB_WEIGHT_OPT_DIS_CH3 Configures whether to disable weight arbitration for TX channel 3.
- 0: Enable
- 1: Disable (R/W)

Register 39.77. H264_DMA_OUT_PUSH_CH3_REG (0x0318)
```

```markdown
| Bit Range | Field Name                          | Description                                                                 |
|-----------|-------------------------------------|-----------------------------------------------------------------------------|
| 31        | Reserved                            |                                                                             |
| 11-10     | H264_DMA_OUTFIFO_PUSH_CH3           | Configures whether to push data into DMA TX FIFO.                           |
| 9         | H264_DMA_OUTFIFO_WDATA_CH3          | Represents the data that needs to be pushed into DMA TX FIFO. (R/W)        |
| 8-0       | Reset                               |                                                                             |

H264_DMA_OUTFIFO_WDATA_CH3 Represents the data that needs to be pushed into DMA TX FIFO. (R/W)

H264_DMA_OUTFIFO_PUSH_CH3 Configures whether to push data into DMA TX FIFO.
- 0: No effect
- 1: Push (R/W/SC)
```