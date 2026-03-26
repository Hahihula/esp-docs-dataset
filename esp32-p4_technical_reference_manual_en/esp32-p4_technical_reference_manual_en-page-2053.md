

```markdown
Register 39.282. H264_DMA_INFIFO_STATUS_CH5_REG (0x0A20)

H264_DMA_INFIFO_FULL_L1_CH5   Represents whether I1 FIFO of RX channel 5 is full.
    0: Not Full
    1: Full
    (RO)

H264_DMA_INFIFO_EMPTY_L1_CH5  Represents whether I1 FIFO of RX channel 5 is empty.
    0: Not empty
    1: Empty
    (RO)

H264_DMA_INFIFO_CNT_L1_CH5    Represents the data quantity in I1 FIFO for RX channel 5. Measurement unit: byte. (RO)
```

```markdown
Register 39.283. H264_DMA_IN_STATE_CH5_REG (0x0A28)

H264_DMA_IN_STATE_CH5   Represents the current control module state machine state for RX channel 5. (RO)

H264_DMA_IN_RESET_AVAIL_CH5  Represents whether it is safe to reset the channel.
    0: Unsafe
    1: Safe
    (RO)
```