
```markdown
Register 4.89: AXI_DMA_OUT_CONFO_CHn_REG(n: 0-2) (0x0148+0x68*n)

AXI_DMA_OUT_RST_CHn   Configures the reset state of TX channel n FSM and TX FIFO pointer.
    0: Release reset
    1: Reset
    (R/W)

AXI_DMA_OUT_LOOP_TEST_CHn   Reserved. (R/W)

AXI_DMA_OUT_AUTO_WRBACK_CHn   Configures whether to enable automatic outlink write-back when all the data in TX FIFO has been transmitted.
    0: Disable
    1: Enable
    (R/W)

AXI_DMA_OUT_EOF_MODE_CHn   Configures when to generate EOF flag.
    0: EOF flag for TX channel n is generated when data to be transmitted has been pushed into FIFO in AXI DMA.
    1: EOF flag for TX channel n is generated when data to be transmitted has been popped from FIFO in AXI DMA.
    (R/W)

AXI_DMA_OUT_ETM_EN_CHn   Configures whether to enable ETM control for TX channel n.
    0: Disable
    1: Enable
    ( R/W )

AXI_DMA_OUT_BURST_SIZE_SEL_CHn   Configures the burst length for TX channel n.
    0: 8 bytes
    1: 16 bytes
    2: 32 bytes
    3: 64 bytes
    4: 128 bytes
    5 ~ 7: Invalid
    (R/W)

AXI_DMA_OUT_CMD_DISABLE_CHn   Configures whether to disable command on TX channel n.
    0: Enable
    1: Disable
    (R/W)
```