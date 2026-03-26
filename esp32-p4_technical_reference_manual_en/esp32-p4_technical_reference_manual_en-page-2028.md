

```markdown
Register 39.227. H264_DMA_INFIFO_STATUS_CHO_REG (0x0514)

| Bit | Field Name                                 | Description                                                                 |
|-----|---------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                                 |                                                                             |
| 30  | (reserved)                                 |                                                                             |
| 29  | H264_DMA_INFIFO_CNT_L3_CHO                 |                                                                             |
| 28  | H264_DMA_INFIFO_EMPTY_L3_CHO               |                                                                             |
| 27  | H264_DMA_INFIFO_FULL_L3_CHO                |                                                                             |
| 26  | (reserved)                                 |                                                                             |
| 25  | H264_DMA_INFIFO_CNT_L2_CHO                 |                                                                             |
| 24  | H264_DMA_INFIFO_EMPTY_L2_CHO               |                                                                             |
| 23  | H264_DMA_INFIFO_FULL_L2_CHO                |                                                                             |
| 22  | (reserved)                                 |                                                                             |
| 21  | H264_DMA_INFIFO_CNT_L1_CHO                 |                                                                             |
| 20  | H264_DMA_INFIFO_EMPTY_L1_CHO               |                                                                             |
| 19  | H264_DMA_INFIFO_FULL_L1_CHO                |                                                                             |
| 18  | Ox0                                        | Reset                                                                        |
| 17  | 1                                           |                                                                                 |
| 16  | 0                                           |                                                                                 |
| 15  | 0                                           |                                                                                 |
| 14  | 0                                           |                                                                                 |
| 13  | Ox0                                        |                                                                                 |
| 12  | 1                                           |                                                                                 |
| 11  | 0                                           |                                                                                 |
| 10  | Ox0                                        |                                                                                 |
| 9   | 1                                           |                                                                                 |
| 8   | 0                                           |                                                                                 |
| 7   | Ox0                                        |                                                                                 |
| 6   | 1                                           |                                                                                 |
| 5   | 0                                           |                                                                                 |
| 4   | Ox0                                        |                                                                                 |
| 3   | 1                                           |                                                                                 |
| 2   | 0                                           |                                                                                 |
| 1   | 1                                           |                                                                                 |
| 0   | Reset                                      |                                                                                 |

H264_DMA_INFIFO_FULL_L2_CHO Represents whether I2 FIFO of RX channel O is full.
O: Not Full
1: Full
(RO)

H264_DMA_INFIFO_EMPTY_L2_CHO Represents whether I2 FIFO of RX channel O is empty.
O: Not empty
1: Empty
(RO)

H264_DMA_INFIFO_CNT_L2_CHO Represents the data quantity in I2 FIFO for RX channel O. Measurement unit: 16 bytes. (RO)

H264_DMA_INFIFO_FULL_L1_CHO Represents whether I1 FIFO of RX channel O is full.
O: Not Full
1: Full
(RO)

H264_DMA_INFIFO_EMPTY_L1_CHO Represents whether I1 FIFO of RX channel O is empty.
O: Not empty
1: Empty
(RO)

H264_DMA_INFIFO_CNT_L1_CHO Represents the data quantity in I1 FIFO for RX channel O. Measurement unit: byte. (RO)

H264_DMA_INFIFO_FULL_L3_CHO Represents whether I3 FIFO of RX channel O is full.
O: Not Full
1: Full
(RO)

H264_DMA_INFIFO_EMPTY_L3_CHO Represents whether I3 FIFO of RX channel O is empty.
O: Not empty
1: Empty
(RO)

H264_DMA_INFIFO_CNT_L3_CHO Represents the data quantity in I3 FIFO for RX channel O. Measurement unit: 8 bytes. (RO)
```