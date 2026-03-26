

```markdown
Register 6.3. DMA2D_OUT_LINK_CONF_CHn_REG (n: 0-3) (0x001C+0x100*n)

DMA2D_OUTLINK_STOP_CHn   Configures whether to stop TX channel n from transmitting data.
    0: Invalid. No effect
    1: Stop
    (R/W/SC)

DMA2D_OUTLINK_START_CHn  Configures whether to enable TX channel n for data transfer.
    0: Disable
    1: Enable
    (R/W/SC)

DMA2D_OUTLINK_RESTART_CHn Configures whether to restart TX channel n for AXI DMA transfer.
    0: Invalid. No effect
    1: Restart
    (R/W/SC)

DMA2D_OUTLINK_PARK_CHn   Represents the status of the transmit descriptor’s FSM.
    0: Running
    1: Idle
    (RO)
```

```markdown
Register 6.4. DMA2D_OUT_LINK_ADDR_CHn_REG (n: 0-3) (0x0020+0x100*n)

DMA2D_OUTLINK_ADDR_CHn   Represents the first transmit descriptor’s address. (R/W)
```