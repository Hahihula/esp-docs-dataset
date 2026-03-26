

```markdown
Register 39.94. H264_DMA_IN_LINK_CONF_CH1_REG (0x061C)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | ... | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|-----|------|---|
|     |    | (reserved) | H264_DMA_INLINK_PARK_CH1 | H264_DMA_INLINK_RESTART_CH1 | H264_DMA_INLINK_STOP_CH1 | H264_DMA_INLINK_START_CH1 | H264_DMA_INLINK_AUTO_RET_CH1 | (reserved) |
|     | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | ... | 0   |

H264_DMA_INLINK_AUTO_RET_CH1 Configures whether to return to the address of the current receive descriptor when there are errors during data reception.
O: Not return
1: Return
(R/W)

H264_DMA_INLINK_STOP_CH1 Configures whether to stop processing the inlink descriptors.
O: No effect
1: Stop
(R/W/SC)

H264_DMA_INLINK_START_CH1 Configures whether to start processing the inlink descriptors.
O: No effect
1: Start
(R/W/SC)

H264_DMA_INLINK_RESTART_CH1 Configures whether to restart a new inlink from the last address.
O: No effect
1: Restart
(R/W/SC)

H264_DMA_INLINK_PARK_CH1 Represents the status of the inlink descriptor's FSM.
O: The inlink descriptor's FSM is working
1: The inlink descriptor's FSM is in idle state
(RO)
```