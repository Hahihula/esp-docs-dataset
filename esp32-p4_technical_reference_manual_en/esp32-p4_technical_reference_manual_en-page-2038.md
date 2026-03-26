

```markdown
Register 39.249. H264_DMA_INFIFO_STATUS_CH2_REG (0x0714)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|--------------------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                |                                                                             |
| 20-18     | H264_DMA_INFIFO_CNT_L3_CH2                 | Represents the data quantity in L3 FIFO for RX channel 2. Measurement unit: 8 bytes. (RO) |
| 19        | H264_DMA_INFIFO_FULL_L3_CH2                | Represents whether L3 FIFO of RX channel 2 is full.<br>0: Not Full<br>1: Full (RO) |
| 17-15     | H264_DMA_INFIFO_EMPTY_L3_CH2               | Represents whether L3 FIFO of RX channel 2 is empty.<br>0: Not empty<br>1: Empty (RO) |
| 16        | (reserved)                                |                                                                             |
| 12-8      | H264_DMA_INFIFO_FULL_L2_CH2                | Represents whether I2 FIFO of RX channel 2 is full.<br>0: Not Full<br>1: Full (RO) |
| 7-5       | H264_DMA_INFIFO_EMPTY_L2_CH2               | Represents whether I2 FIFO of RX channel 2 is empty.<br>0: Not empty<br>1: Empty (RO) |
| 4-2       | H264_DMA_INFIFO_CNT_L2_CH2                 | Represents the data quantity in I2 FIFO for RX channel 2. Measurement unit: 16 bytes. (RO) |
| 1        | Reset                                     |                                                                             |
| 0         | H264_DMA_INFIFO_FULL_L1_CH2                | Represents whether I1 FIFO of RX channel 2 is full.<br>0: Not Full<br>1: Full (RO) |
|           |                                          |                                                                             |
|           | H264_DMA_INFIFO_EMPTY_L1_CH2               | Represents whether I1 FIFO of RX channel 2 is empty.<br>0: Not empty<br>1: Empty (RO) |
|           |                                          |                                                                             |
|           | H264_DMA_INFIFO_CNT_L1_CH2                 | Represents the data quantity in I1 FIFO for RX channel 2. Measurement unit: byte. (RO) |
|           |                                          |                                                                             |
|           | H264_DMA_INFIFO_FULL_L3_CH2                | Represents whether L3 FIFO of RX channel 2 is full.<br>0: Not Full<br>1: Full (RO) |
|           |                                          |                                                                             |
|           | H264_DMA_INFIFO_EMPTY_L3_CH2               | Represents whether L3 FIFO of RX channel 2 is empty.<br>0: Not empty<br>1: Empty (RO) |
|           |                                          |                                                                             |
|           | H264_DMA_INFIFO_CNT_L3_CH2                 | Represents the data quantity in L3 FIFO for RX channel 2. Measurement unit: 8 bytes. (RO) |
```