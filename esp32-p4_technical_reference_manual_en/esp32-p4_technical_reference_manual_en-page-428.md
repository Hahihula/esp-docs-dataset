

```markdown
Register 6.1. DMA2D_OUT_CONFO_CHn_REG (n: 0-3) (0x0000+0x100*n)

Continued from the previous page...

DMA2D_OUT_CMD_DISABLE_CHn Configures reset command for TX channel n.
    0: Set 0 after reset release
    1: Pause transfers before reset
    (R/W)

DMA2D_OUT_ARB_WEIGHT_OPT_DIS_CHn Configures whether to enable weight optimization for TX channel n.
    0: Enable
    1: Disable
    (R/W)

Register 6.2. DMA2D_OUT_PUSH_CHn_REG (n: 0-3) (0x0018+0x100*n)
```

```markdown
DMA2D_OUTFIFO_WDATA_CHn Configures the data to be pushed into the 2D-DMA TX FIFO. (R/W)

DMA2D_OUTFIFO_PUSH_CHn Configures whether to push data into the 2D-DMA TX FIFO.
    0: Not push 1: Push
    (R/W/SC)
```