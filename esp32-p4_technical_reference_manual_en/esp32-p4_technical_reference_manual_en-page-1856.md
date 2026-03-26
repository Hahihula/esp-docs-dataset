

```markdown
- The video frame to be encoded is P frame:
    (a) Clear H264 interrupts and enable interrupts.
    (b) Start H264_DMA TX channel 0: Refer to section 39.5.2.3 for the configuration.
    (c) Start H264_DMA RX channel 0 and RX channel 1: Refer to section 39.5.2.3 for the configuration.
    (d) Start H264_DMA RX channel 2: Refer to section 39.5.2.3 for the configuration.
    (e) Start H264_DMA RX channel 4: Refer to section 39.5.2.3 for the configuration.
    (f) Start H264_DMA RX channel 5: Refer to section 39.5.2.3 for the configuration.
    (g) Start H264_DMA TX channel 3 and TX channel 4: Refer to section 39.5.2.3 for the configuration.
    (h) To use the MV merge function, start H264_DMA RX channel 3: Refer to section 39.5.2.3 for the configuration.
    (i) Start H264_DMA to move the reference picture from external memory to internal memory: Write 1 to register `H264_DMA_MOVE_START`.
    (j) Wait for H264_DMA_MOVE_2MB_LINE_DONE_INT interrupt. When the interrupt is triggered, start H264_DMA_TX channel 1. Refer to section 39.5.2.3 for the configuration.
    (k) Start encoding of a picture: Write 1 to register `H264_FRAME_START`.
    (l) Wait for the H264_DB_TMP_READY_INT interrupt. When the interrupt is triggered, start H264_DMA_TX channel 2. Refer to section 39.5.2.3 for the configuration.
    (m) Wait for the H264_FRAME_DONE_INT interrupt. When the interrupt is triggered, it indicates that the picture encoding is completed.
    (n) Make sure the data is written completely referring to section 39.5.2.4.
    (o) Reset each sending and receiving channel of H264_DMA referring to section 39.5.2.4.
    (p) Reset the read and write counter of the deblocking filter intermediate data and the read and write counter of the reference picture data in H264_DMA. To be specific, set the register `H264_DMA_RX_CH2_INTER_COUNTER_RST` to 1, and then set it to 0; Set the register `H264_DMA_RX_CH5_INTER_COUNTER_RST` to 1 and then set it to 0.
- After any frame ends, the following registers corresponding to the currently encoded video sequence can be reconfigured:
    - Registers related to the quantization result decimate function, refer to the description in chapter 39.5.1.2.
    - Registers related to the MB level rate control function, refer to the description in chapter 39.5.1.4.
    - Deblocking filter enable register: `H264_A_BYPASS_DB_FILTER`.
    - ROI function related registers, refer to the description in chapter 39.5.1.5.
    - Registers related to the slice header information: `H264_SLICE_RMEAIN_BIT`, `H264_SLICE_REMAIN_BITLENGTH`, `H264_SLICE_BYTE_LENGTH`, `H264_SLICE_BYTE_LSB`, and `H264_SLICE_BYTE_MSB`.
```