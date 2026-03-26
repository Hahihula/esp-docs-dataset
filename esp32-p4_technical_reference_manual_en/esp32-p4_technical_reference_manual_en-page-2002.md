
```markdown
Register 39174. H264_DMA_OUTFIFO_STATUS_CHO_REG (0x0014)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    | 0x0| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0x0| 1 | 0 | OxO| 1 | 0 | Reset |

H264_DMA_OUTFIFO_FULL_L2_CHO Represents whether I2 FIFO of TX channel O is full.
- 0: Not Full
- 1: Full (RO)

H264_DMA_OUTFIFO_EMPTY_L2_CHO Represents whether I2 FIFO of TX channel O is empty.
- 0: Not empty
- 1: Empty (RO)

H264_DMA_OUTFIFO_CNT_L2_CHO Represents the data quantity in I2 FIFO for TX channel O. Measurement unit: 16 bytes. (RO)

H264_DMA_OUTFIFO_FULL_L1_CHO Represents whether I1 FIFO of TX channel O is full.
- 0: Not Full
- 1: Full (RO)

H264_DMA_OUTFIFO_EMPTY_L1_CHO Represents whether I1 FIFO of TX channel O is empty.
- 0: Not empty
- 1: Empty (RO)

H264_DMA_OUTFIFO_CNT_L1_CHO Represents the data quantity in I1 FIFO for TX channel O. Measurement unit: byte. (RO)

H264_DMA_OUTFIFO_FULL_L3_CHO Represents whether I3 FIFO of TX channel O is full.
- 0: Not Full
- 1: Full (RO)

H264_DMA_OUTFIFO_EMPTY_L3_CHO Represents whether I3 FIFO of TX channel O is empty.
- 0: Not empty
- 1: Empty (RO)

H264_DMA_OUTFIFO_CNT_L3_CHO Represents the data quantity in I3 FIFO for TX channel O. Measurement unit: 8 bytes. (RO)
```