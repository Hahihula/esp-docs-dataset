

```markdown
Register 4.15. AHB_DMA_OUT_CONFO_CHn_REG (n: 0-2) (0x00D0+0xC0*n)

AHB_DMA_OUT_RST_CHn Configures the reset state of TX channel n FSM and TX FIFO pointer.
O: Release reset
1: Reset
(R/W)

AHB_DMA_OUT_LOOP_TEST_CHn Reserved. (R/W)

AHB_DMA_OUT_AUTO_WRBACK_CHn Configures whether to enable automatic outlink write-back when all the data in TX FIFO has been transmitted.
O: Disable
1: Enable
(R/W)

AHB_DMA_OUT_EOF_MODE_CHn Configures when to generate EOF flag.
O: EOF flag for TX channel n is generated when data to be transmitted has been pushed into FIFO in AHB DMA.
1: EOF flag for TX channel n is generated when data to be transmitted has been popped from FIFO in AHB DMA.
(R/W)

AHB_DMA_OUTDSCR_BURST_EN_CHn Configures whether to enable INCR burst transfer for TX channel n reading descriptors.
O: Disable
1: Enable
(R/W)

AHB_DMA_OUT_DATA_BURST_EN_CHn Configures whether to enable INCR burst transfer for TX channel n.
O: Disable
1: Enable
(R/W)

AHB_DMA_OUT_ETM_EN_CHn Configures whether to enable ETM control for TX channel n.
O: Disable
1: Enable
(R/W)
```