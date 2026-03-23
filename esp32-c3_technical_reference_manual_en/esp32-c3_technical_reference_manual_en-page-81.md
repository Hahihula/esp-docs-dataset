

```markdown
Register 2.11. GDMA_OUT_CONFO_CHn_REG (n: 0-2) (0x00D0+192*n)

31 | 6 | 5 | 4 | 3 | 2 | 1 | 0
---|----|----|----|----|----|----|----
0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Reset

GDMA_OUT_RST_CHn    This bit is used to reset GDMA channel O TX FSM and TX FIFO pointer. (R/W)

GDMA_OUT_LOOP_TEST_CHn Reserved. (R/W)

GDMA_OUT_AUTO_WRBACK_CHn Set this bit to enable automatic outlink-writeback when all the data in TX buffer has been transmitted. (R/W)

GDMA_OUT_EOF_MODE_CHn EOF flag generation mode when transmitting data. 1: EOF flag for TX channel O is generated when data need to transmit has been popped from FIFO in GDMA. (R/W)

GDMA_OUTDSR_BURST_EN_CHn Set this bit to 1 to enable INCR burst transfer for TX channel O reading descriptor when accessing internal RAM. (R/W)

GDMA_OUT_DATA_BURST_EN_CHn Set this bit to 1 to enable INCR burst transfer for TX channel O transmitting data when accessing internal RAM. (R/W)

Register 2.12. GDMA_OUT_CONF1_CHn_REG (n: 0-2) (0x00D4+192*n)

31 | 13 | 12 | 11 | 0
---|-----|-----|----|----
0 | 0 | 0 | 0 | Reset

GDMA_OUT_CHECK_OWNER_CHn Set this bit to enable checking the owner attribute of the descriptor. (R/W)
```