

```markdown
Register 39.109. H264_DMA_IN_LINK_CONF_CH4_REG (0x091C)

H264_DMA_INLINK_AUTO_RET_CH4 Configures whether to return to the address of the current receive descriptor when there are errors during data reception.
O: No return
1: Return
(R/W)

H264_DMA_INLINK_STOP_CH4 Configures whether to stop processing the inlink descriptors.
O: No effect
1: Stop
(R/W/SC)

H264_DMA_INLINK_START_CH4 Configures whether to start processing the inlink descriptors.
O: No effect
1: Start
(R/W/SC)

H264_DMA_INLINK_RESTART_CH4 Configures whether to restart a new inlink from the last address.
O: No effect
1: Restart
(R/W/SC)

H264_DMA_INLINK_PARK_CH4 Represents the status of the inlink descriptor's FSM.
O: The inlink descriptor's FSM is working
1: The inlink descriptor's FSM is in idle state
(RO)
```