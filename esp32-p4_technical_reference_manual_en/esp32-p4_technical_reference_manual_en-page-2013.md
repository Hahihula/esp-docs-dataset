
```markdown
Register 39195. H264_DMA_OUTFIFO_STATUS_CH2_REG (0x0214)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved                                                                     |
| 30  | H264_DMA_OUTFIFO_CNT_L3_CH2                                                 |
| 29  | H264_DMA_OUTFIFO_FULL_L3_CH2                                                |
| 28  | H264_DMA_OUTFIFO_EMPTY_L3_CH2                                               |
| 27  | reserved                                                                     |
| 26  | H264_DMA_OUTFIFO_CNT_L2_CH2                                                 |
| 25  | H264_DMA_OUTFIFO_FULL_L2_CH2                                                |
| 24  | H264_DMA_OUTFIFO_EMPTY_L2_CH2                                               |
| 23  | reserved                                                                     |
| 22  | H264_DMA_OUTFIFO_CNT_L1_CH2                                                 |
| 21  | H264_DMA_OUTFIFO_FULL_L1_CH2                                                |
| 20  | H264_DMA_OUTFIFO_EMPTY_L1_CH2                                               |
| 19  | Ox0                                                                          |
| 18  | 1                                                                            |
| 17  | 0                                                                            |
| 16  | Ox0                                                                          |
| 15  | 1                                                                            |
| 14  | 0                                                                            |
| 13  | Ox0                                                                          |
| 12  | 1                                                                            |
| 11  | 0                                                                            |
| 10  | Reset                                                                        |

H264_DMA_OUTFIFO_FULL_L2_CH2 Represents whether I2 FIFO of TX channel 2 is full.
O: Not Full
1: Full (RO)

H264_DMA_OUTFIFO_EMPTY_L2_CH2 Represents whether I2 FIFO of TX channel 2 is empty.
O: Not empty
1: Empty (RO)

H264_DMA_OUTFIFO_CNT_L2_CH2 Represents the data quantity in I2 FIFO for TX channel 2. Measurement unit: 16 bytes. (RO)

H264_DMA_OUTFIFO_FULL_L1_CH2 Represents whether I1 FIFO of TX channel 2 is full.
O: Not Full
1: Full (RO)

H264_DMA_OUTFIFO_EMPTY_L1_CH2 Represents whether I1 FIFO of TX channel 2 is empty.
O: Not empty
1: Empty (RO)

H264_DMA_OUTFIFO_CNT_L1_CH2 Represents the data quantity in I1 FIFO for TX channel 2. Measurement unit: byte. (RO)

H264_DMA_OUTFIFO_FULL_L3_CH2 Represents whether I3 FIFO of TX channel 2 is full.
O: Not Full
1: Full (RO)

H264_DMA_OUTFIFO_EMPTY_L3_CH2 Represents whether I3 FIFO of TX channel 2 is empty.
O: Not empty
1: Empty (RO)

H264_DMA_OUTFIFO_CNT_L3_CH2 Represents the data quantity in I3 FIFO for TX channel 2. Measurement unit: 8 bytes. (RO)
```