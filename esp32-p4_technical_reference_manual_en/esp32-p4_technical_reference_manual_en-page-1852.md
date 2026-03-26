

```markdown
(h) To use the MB level rate control function, configure its related registers referring to the description in section 39.5.1.4.
(i) To use the ROI function, configure its related registers referring to the description in chapter 39.5.1.5.
(j) To use the MV merge function, configure its related registers referring to the description in section 39.5.1.3.

3. Perform the corresponding operations based on the type of video frame to be encoded (In a GOP, the first frame is an I frame, and subsequent frames are P frames):

• The video frame to be encoded is an I frame:

(a) Start H264_DMA TX channel 0: Refer to chapter 39.5.2.3 for the configuration.
(b) Start H264_DMA RX channel 0 and RX channel 1: Refer to chapter 39.5.2.3 for the configuration.
(c) Start H264_DMA RX channel 2: Refer to chapter 39.5.2.3 for the configuration.
(d) To use the MV merge function, start H264_DMA RX channel 3. Refer to chapter 39.5.2.3 for the configuration.
(e) Start H264_DMA RX channel 4: Refer to chapter 39.5.2.3 for the configuration.
(f) Clear H264 interrupts and enable interrupts.
(g) Start the encoding of a picture: Write 1 to register H264_FRAME_START.
(h) Wait for the H264_DB_TMP_READY_INT interrupt. When the interrupt is triggered, start H264_DMA TX channel 2. Refer to chapter 39.5.2.3 for the configuration.
(i) Wait for the H264_REC_READY_INT interrupt. When the interrupt is triggered, start H264_DMA RX channel 5, H264_DMA TX channel 3, and TX channel 4. Refer to section 39.5.2.3 for the configuration.
(j) Start H264_DMA to move the reference picture from external memory to internal memory: Write 1 to register H264_DMA_MOVE_START.
(k) Wait for the H264_DMA_MOVE_2MB_LINE_DONE_INT interrupt. When the interrupt is triggered, start H264_DMA TX channel 1. Refer to chapter 39.5.2.3 for the configuration.
(l) Wait for the H264_FRAME_DONE_INT interrupt. When the interrupt is triggered, it indicates that the picture encoding is completed.
(m) Reset H264_DMA TX channel 2 and RX channel 2: Refer to chapter 39.5.2.4 for the configuration.
(n) Reset the read and write time counter of the deblocking filter intermediate data in H264_DMA: Set register H264_DMA_RX_CH2_INTER_COUNTER_RST to 1, then set to 0.

• The video frame to be encoded is P frame:

(a) Clear H264 interrupts and enable interrupts.
(b) Start H264_DMA RX channel 2: Refer to chapter 39.5.2.3 for the configuration.
(c) Start encoding a picture: Write 1 to register H264_FRAME_START.
```