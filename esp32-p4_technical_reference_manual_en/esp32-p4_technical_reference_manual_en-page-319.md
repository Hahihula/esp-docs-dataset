

```markdown
Register 4.92. AXI_DMA_OUT_LINK1_CHn_REG (n: 0-2) (0x0158+0x68*n)

AXI_DMA_OUTLINK_STOP_CHn   Configures whether to stop TX channel n from transmitting data.
    0: Invalid. No effect
    1: Stop
        (WT)

AXI_DMA_OUTLINK_START_CHn   Configures whether to enable TX channel n for data transfer.
    0: Disable
    1: Enable
        (WT)

AXI_DMA_OUTLINK_RESTART_CHn  Configures whether to restart TX channel n for AXI DMA transfer.
    0: Invalid. No effect
    1: Restart
        (WT)

AXI_DMA_OUTLINK_PARK_CHn     Represents the status of the transmit descriptor's FSM.
    0: Running
    1: Idle
        (RO)
```

Register 4.93. AXI_DMA_OUT_LINK2_CHn_REG (n: 0-2) (0x015C+0x68*n)

AXI_DMA_OUTLINK_ADDR_CHn     Represents the first transmit descriptor's address. (R/W)
```