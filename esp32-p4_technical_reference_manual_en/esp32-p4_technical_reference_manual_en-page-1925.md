
```markdown
Chapter 39 H264 Encoder

Register 39.83. H264_DMA_OUT_LINK_CONF_CH4_REG (0x041C)

H264_DMA_OUTLINK_STOP_CH4   Configures whether to stop processing the outlink descriptors.
O: No effect
1: Stop
(R/W/SC)

H264_DMA_OUTLINK_START_CH4  Configures whether to start processing the outlink descriptors.
O: No effect
1: Start
(R/W/SC)

H264_DMA_OUTLINK_RESTART_CH4 Configures whether to restart a new outlink from the last address.
O: No effect
1: Restart
(R/W/SC)

H264_DMA_OUTLINK_PARK_CH4   Represents the status of the transmit descriptor’s FSM.
O: The outlink descriptor’s FSM is working
1: The outlink descriptor’s FSM is in idle state
(RO)

Register 39.84. H264_DMA_OUT_LINK_ADDR_CH4_REG (0x0420)

H264_DMA_OUTLINK_ADDR_CH4   Configures the first outlink descriptor’s address. (R/W)
```