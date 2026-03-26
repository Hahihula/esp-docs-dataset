

```markdown
Register 4.14. AHB_DMA_IN_LINK_CHn_REG (n: 0-2) (0x0080+0xC0*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 5   | AHB_DMA_INLINK_AUTO_RET_CHn                                                |
| 4   | AHB_DMA_INLINK_STOP_CHn                                                    |
| 3   | AHB_DMA_INLINK_START_CHn                                                   |
| 2   | AHB_DMA_INLINK_RESTART_CHn                                                 |
| 1   | AHB_DMA_INLINK_PARK_CHn                                                     |
| 0   | Reset                                                                      |

AHB_DMA_INLINK_AUTO_RET_CHn Configures whether to return to the current receive descriptor’s address when there are some errors in current receiving data.
- O: Not return
- 1: Return (R/W)

AHB_DMA_INLINK_STOP_CHn Configures whether to stop RX channel n from receiving data.
- O: Invalid. No effect
- 1: Stop (WT)

AHB_DMA_INLINK_START_CHn Configures whether to enable RX channel n for data transfer.
- O: Disable
- 1: Enable (WT)

AHB_DMA_INLINK_RESTART_CHn Configures whether to restart RX channel n for AHB DMA transfer.
- O: Invalid. No effect
- 1: Restart (WT)

AHB_DMA_INLINK_PARK_CHn Represents the status of the receive descriptor’s FSM.
- O: Running
- 1: Idle (RO)
```