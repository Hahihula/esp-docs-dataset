

```markdown
(h) To use the MB level rate control function, configure its related registers referring to chapter 39.5.1.4.
(i) To use the ROI function, configure its related registers referring to chapter 39.5.1.5.
(j) To use the MV merge function, configure its related registers referring to chapter 39.5.1.3.

2. According to whether the frame to be encoded belongs to video sequence A or B, use the information corresponding to the video sequence and configure each H264_DMA channel referring to section 39.5.2.5:

(a) Configure H264_DMA TX channel 0.
(b) Configure H264_DMA TX channel 1.
(c) Configure H264_DMA TX channel 2.
(d) Configure H264_DMA TX channel 3 and TX channel 4.
(e) Configure H264_DMA RX channel 0 and RX channel 1.
(f) Configure H264_DMA RX channel 2.
(g) Configure H264_DMA RX channel 3.
(h) Configure H264_DMA RX channel 4.
(i) Configure H264_DMA RX channel 5.

3. Perform the corresponding operations based on the type of video frame to be encoded. Video sequence A and B are encoded alternately, i.e., first a picture in video sequence A is encoded, and then a picture in video sequence B, etc. In a GOP, the first frame is an I frame, and the subsequent frames are P frames for any video sequence.

• The video frame to be encoded is an I frame:

(a) Start H264_DMA TX channel 0: Refer to section 39.5.2.3 for the configuration.
(b) Start H264_DMA RX channel 0 and RX channel 1: Refer to section 39.5.2.3 for the configuration.
(c) Start H264_DMA RX channel 2: Refer to section 39.5.2.3 for the configuration.
(d) Start H264_DMA RX channel 4: Refer to section 39.5.2.3 for the configuration.
(e) Clear H264 interrupts and enable interrupts.
(f) Start encoding a picture: Write 1 to register H264_FRAME_START.
(g) Wait for the H264_DB_TMP_READY_INT interrupt. When the interrupt is triggered, start H264_DMA TX channel 2. Refer to section 39.5.2.3 for the configuration.
(h) Wait for the H264_FRAME_DONE_INT interrupt. When the interrupt is triggered, it means that the picture encoding is completed.
(i) Make sure the data is written completely. Refer to section 39.5.2.4 for the method.
(j) Reset each sending and receiving channel of H264_DMA referring to section 39.5.2.4.
(k) Reset the read and write counter of the deblocking filter intermediate data, and the read and write counter of the reference picture data in H264_DMA. To be specific, set register H264_DMA_RX_CH2_INTER_COUNTER_RST to 1, and then set it to 0. Set the register H264_DMA_RX_CH5_INTER_COUNTER_RST is set to 1 and then set it to 0.
```