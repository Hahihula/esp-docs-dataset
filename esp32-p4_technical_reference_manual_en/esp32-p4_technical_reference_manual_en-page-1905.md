

```markdown
Chapter 39 H264 Encoder

Register 39.60. H264_DMA_OUT_LINK_CONF_CHO_REG (0x001C)

H264_DMA_OUTLINK_STOP_CHO Configures whether to stop processing the outlink descriptors.
O: No effect
1: Stop
(R/W/SC)

H264_DMA_OUTLINK_START_CHO Configures whether to start processing the outlink descriptors.
O: No effect
1: Start
(R/W/SC)

H264_DMA_OUTLINK_RESTART_CHO Configures whether to restart a new outlink from the last address.
O: No effect
1: Restart
(R/W/SC)

H264_DMA_OUTLINK_PARK_CHO Represents the status of the transmit descriptor's FSM.
O: The outlink descriptor's FSM is working
1: The outlink descriptor's FSM is in idle state
(RO)
```

```markdown
Register 39.61. H264_DMA_OUT_LINK_ADDR_CHO_REG (0x0020)

H264_DMA_OUTLINK_ADDR_CHO Configures the first outlink descriptor's address. (R/W)
```