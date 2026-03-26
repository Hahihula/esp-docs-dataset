

```markdown
– Registers related to the MV merge function, refer to the description in chapter 39.5.1.3.
4. Repeat steps 2 and 3 until one GOP of each of the 2 video sequences is encoded.
5. Reset the read and write times counter of the deblocking filter result data in H264_DMA. To be specific, set the register H264_DMA_RX_CHO_EXTER_COUNTER_RST to 1, then set to 0. Set the register H264_DMA_RX_CH1_EXTER_COUNTER_RST to 1, then set to 0.
6. Reconfigure from step 1 to start the encoding of the next GOP.

39.7.3 Soft Reset

No matter what working mode H264 is in, reset it according to the following process can stop encoding at any time.

1. Reset ENC_CORE: Write 1 to register H264_SYS_RST_PULSE.
2. Reset each sending and receiving channel of H264_DMA referring to section 39.5.2.4.
3. Reset each read and write time counter in H264_DMA. To be specific, set register
   H264_DMA_RX_CHO_EXTER_COUNTER_RST to 1, then set it to 0; Set register
   H264_DMA_RX_CH1_EXTER_COUNTER_RST to 1, then set it to 0; Set the register
   H264_DMA_RX_CH2_INTER_COUNTER_RST to 1, and then set it to 0; Set the register
   H264_DMA_RX_CH5_INTER_COUNTER_RST to 1, and then set it to 0.
4. H264 returns to the initial state and can be reconfigured as needed.
```