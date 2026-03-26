

```markdown
Register 39.73. H264_DMA_OUT_LINK_CONF_CH2_REG (0x021C)

H264_DMA_OUTLINK_STOP_CH2 Configures whether to stop processing outlink descriptors.
O: No effect
1: Stop
(R/W/SC)

H264_DMA_OUTLINK_START_CH2 Configures whether to start processing outlink descriptors.
O: No effect
1: Start
(R/W/SC)

H264_DMA_OUTLINK_RESTART_CH2 Configures whether to restart a new outlink from the last address.
O: No effect
1: Restart
(R/W/SC)

H264_DMA_OUTLINK_PARK_CH2 Represents the status of the transmit descriptor's FSM.
O: The outlink descriptor's FSM is working
1: The outlink descriptor's FSM is in idle state
(RO)
```

```markdown
Register 39.74. H264_DMA_OUT_LINK_ADDR_CH2_REG (0x0220)

H264_DMA_OUTLINK_ADDR_CH2 Configures the first outlink descriptor's address. (R/W)
```