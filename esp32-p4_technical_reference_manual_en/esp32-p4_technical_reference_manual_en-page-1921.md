

```markdown
Register 39.78. H264_DMA_OUT_LINK_CONF_CH3_REG (0x031C)

H264_DMA_OUTLINK_STOP_CH3 Configures whether to stop processing the outlink descriptors.
O: No effect
1: Stop
(R/W/SC)

H264_DMA_OUTLINK_START_CH3 Configures whether to start processing the outlink descriptors.
O: No effect
1: Start
(R/W/SC)

H264_DMA_OUTLINK_RESTART_CH3 Configures whether to restart a new outlink from the last address.
O: No effect
1: Restart
(R/W/SC)

H264_DMA_OUTLINK_PARK_CH3 Represents the status of the transmit descriptor's FSM.
O: The outlink descriptor's FSM is working
1: The outlink descriptor's FSM is in idle state
(RO)
```

```markdown
Register 39.79. H264_DMA_OUT_LINK_ADDR_CH3_REG (0x0320)

H264_DMA_OUTLINK_ADDR_CH3 Configures the first outlink descriptor's address. (R/W)
```