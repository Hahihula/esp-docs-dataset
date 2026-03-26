
```markdown
Register 39.260. H264_DMA_INFIFO_STATUS_CH3_REG (0x0814)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31-20     | (reserved)                                |                                                                             |
| 19        | H264_DMA_INFIFO_CNT_L3_CH3                | Represents the data quantity in L3 FIFO for RX channel 3. Measurement unit: 8 bytes. (RO) |
| 18        | H264_DMA_INFIFO_EMPTY_L3_CH3              | Represents whether L3 FIFO of RX channel 3 is empty.<br>0: Not empty<br>1: Empty (RO) |
| 17-15     | H264_DMA_INFIFO_FULL_L3_CH3               | Represents whether L3 FIFO of RX channel 3 is full.<br>0: Not Full<br>1: Full (RO) |
| 14        | (reserved)                                |                                                                             |
| 13-8      | Ox0                                       |                                                                             |
| 7         | H264_DMA_INFIFO_CNT_L1_CH3                | Represents the data quantity in L1 FIFO for RX channel 3. Measurement unit: byte. (RO) |
| 6         | H264_DMA_INFIFO_EMPTY_L1_CH3              | Represents whether L1 FIFO of RX channel 3 is empty.<br>0: Not empty<br>1: Empty (RO) |
| 5-2       | Ox0                                       |                                                                             |
| 1         | H264_DMA_INFIFO_FULL_L1_CH3               | Represents whether L1 FIFO of RX channel 3 is full.<br>0: Not Full<br>1: Full (RO) |
| 0         | Reset                                     |                                                                             |

H264_DMA_INFIFO_FULL_L2_CH3   Represents whether I2 FIFO of RX channel 3 is full.
    0: Not Full
    1: Full
    (RO)

H264_DMA_INFIFO_EMPTY_L2_CH3  Represents whether I2 FIFO of RX channel 3 is empty.
    0: Not empty
    1: Empty
    (RO)

H264_DMA_INFIFO_CNT_L2_CH3    Represents the data quantity in I2 FIFO for RX channel 3. Measurement unit: 16 bytes. (RO)

H264_DMA_INFIFO_FULL_L1_CH3   Represents whether I1 FIFO of RX channel 3 is full.
    0: Not Full
    1: Full
    (RO)

H264_DMA_INFIFO_EMPTY_L1_CH3  Represents whether I1 FIFO of RX channel 3 is empty.
    0: Not empty
    1: Empty
    (RO)

H264_DMA_INFIFO_CNT_L1_CH3    Represents the data quantity in I1 FIFO for RX channel 3. Measurement unit: byte. (RO)

H264_DMA_INFIFO_FULL_L3_CH3   Represents whether I3 FIFO of RX channel 3 is full.
    0: Not Full
    1: Full
    (RO)

H264_DMA_INFIFO_EMPTY_L3_CH3  Represents whether I3 FIFO of RX channel 3 is empty.
    0: Not empty
    1: Empty
    (RO)

H264_DMA_INFIFO_CNT_L3_CH3    Represents the data quantity in I3 FIFO for RX channel 3. Measurement unit: 8 bytes. (RO)
```