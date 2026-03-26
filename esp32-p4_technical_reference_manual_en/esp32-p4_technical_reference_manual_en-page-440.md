

```markdown
Register 6.19. DMA2D_IN_LINK_CONF_CHn_REG (n: 0-2) (0x051C+0x100*n)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 1  | 0  | 0  | Reset |

DMA2D_INLINK_AUTO_RET_CHn Configure the value of the owner bit written back to the receive descriptor.
O: Write back 0
1: Write back 1
(R/W)

DMA2D_INLINK_STOP_CHn Configures whether to stop RX channel n from receiving data.
O: Invalid. No effect
1: Stop
(R/W/SC)

DMA2D_INLINK_START_CHn Configures whether to enable RX channel n for data transfer.
O: Disable
1: Enable
(R/W/SC)

DMA2D_INLINK_RESTART_CHn Configures whether to restart RX channel n for 2D-DMA transfer.
O: Invalid. No effect
1: Restart
(R/W/SC)

DMA2D_INLINK_PARK_CHn Represents the status of the receive descriptor's FSM.
O: Running
1: Idle
(RO)
```