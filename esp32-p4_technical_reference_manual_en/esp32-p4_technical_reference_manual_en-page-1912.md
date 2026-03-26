

```markdown
Register 39.68. H264_DMA_OUT_LINK_CONF_CH1_REG (0x011C)

H264_DMA_OUTLINK_STOP_CH1 Configures whether to stop processing the outlink descriptors.
O: No effect
1: Stop
(R/W/SC)

H264_DMA_OUTLINK_START_CH1 Configures whether to start processing the outlink descriptors.
O: No effect
1: Start
(R/W/SC)

H264_DMA_OUTLINK_RESTART_CH1 Configures whether to restart a new outlink from the last address.
O: No effect
1: Restart
(R/W/SC)

H264_DMA_OUTLINK_PARK_CH1 Represents the status of the transmit descriptor's FSM.
O: The outlink descriptor's FSM is working
1: The outlink descriptor's FSM is in idle state
(RO)
```

Register 39.69. H264_DMA_OUT_LINK_ADDR_CH1_REG (0x0120)

```markdown
H264_DMA_OUTLINK_ADDR_CH1 Configures the first outlink descriptor's address. (R/W)
```