

```markdown
Register 39.180. H264_DMA_OUT_RO_STATUS_CHO_REG (0x0040)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-18     | (reserved)                                |                                                                             |
| 17        | H264_DMA_OUT_BURST_BLOCK_NUM_CHO           | Represents the number of burst blocks.                                     |
| 14        | H264_DMA_OUT_PIXEL_BYTE_CHO                | Represents the pixel byte count per channel.                                |
| 13-8      | H264_DMA_OUT_RO_RD_STATE_CHO               | Represents the state of reading RAM for reorder. (RO)                       |
| 7         | H264_DMA_OUT_RO_WR_STATE_CHO               | Represents the state of writing RAM for reorder. (RO)                       |
| 6-0       | H264_DMA_OUTFIFO_RO_CNT_CHO                | Represents the 8-byte number of data in the reordered TX FIFO for channel 0. (RO) |

H264_DMA_OUTFIFO_RO_CNT_CHO Represents the 8-byte number of the data in the reordered TX FIFO for channel 0. (RO)

H264_DMA_OUT_RO_WR_STATE_CHO Represents the state of writing RAM for reorder. (RO)

H264_DMA_OUT_RO_RD_STATE_CHO Represents the state of reading RAM for reorder. (RO)

H264_DMA_OUT_PIXEL_BYTE_CHO Represents the number of bytes contained in a pixel at TX channel 0.
- 0: 1 byte
- 1: 1.5 bytes
- 2: 2 bytes
- 3: 2.5 bytes
- 4: 3 bytes
- 5: 4 bytes (RO)

H264_DMA_OUT_BURST_BLOCK_NUM_CHO Reserved. (RO)
```

Register 39.181. H264_DMA_OUT_BUF_LEN_CHO_REG (0x0070)

```markdown
| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-13     | (reserved)                                |                                                                             |
| 12        | H264_DMA_OUT_CMDFIFO_BUF_LEN_HB_CHO        | Represents the remaining request data. (RO)                                 |

H264_DMA_OUT_CMDFIFO_BUF_LEN_HB_CHO Represents the remaining request data. (RO)
```