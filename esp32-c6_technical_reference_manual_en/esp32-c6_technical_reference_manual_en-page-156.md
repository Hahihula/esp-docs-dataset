

```markdown
Register 4.15. GDMA_OUT_CONFO_CHn_REG (n: 0-2) (0x00D0+0xC0*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | GDMA_OUT_ETM_EN_CHn | GDMA_OUT_DATA_BURST_EN_CHn | GDMA_OUT_OUDSCR_BURST_EN_CHn | GDMA_OUT_EOF_MODE_CHn | GDMA_OUT_AUTO_WRBACK_CHn | GDMA_OUT_LOOP_TEST_CHn | Reset |
```

GDMA_OUT_RST_CHn Configures the reset state of GDMA channel n TX FSM and TX FIFO pointer.
- 0: Release reset
- 1: Reset
(R/W)

GDMA_OUT_LOOP_TEST_CHn Reserved. (R/W)

GDMA_OUT_AUTO_WRBACK_CHn Configures whether or not to enable automatic outlink write-back when all the data in TX FIFO has been transmitted.
- 0: Disable
- 1: Enable
(R/W)

GDMA_OUT_EOF_MODE_CHn Configures when to generate EOF flag.
- 0: EOF flag for TX channel n is generated when data to be transmitted has been pushed into FIFO in GDMA.
- 1: EOF flag for TX channel n is generated when data to be transmitted has been popped from FIFO in GDMA.
(R/W)

GDMA_OUT_OUDSCR_BURST_EN_CHn Configures whether or not to enable INCR burst transfer for TX channel n reading descriptors.
- 0: Disable
- 1: Enable
(R/W)

GDMA_OUT_DATA_BURST_EN_CHn Configures whether or not to enable INCR burst transfer for TX channel n.
- 0: Disable
- 1: Enable
(R/W)

GDMA_OUT_ETM_EN_CHn Configures whether or not to enable ETM control for TX channel n.
- 0: Disable
- 1: Enable
( (R/W)
```