

```markdown
Register 2.7. GDMA_IN_CONF0_CHn_REG (n: 0-2) (0x0070+192*n)

31 | (reserved) | 5 | 4 | 3 | 2 | 1 | 0
---|------------|---|---|---|---|---|---
0 | 0 | 0 | 0 | 0 | 0 | 0 | 0

GDMA_IN_RST_CHn This bit is used to reset GDMA channel O RX FSM and RX FIFO pointer. (R/W)

GDMA_IN_LOOP_TEST_CHn This bit is used to fill the owner bit of receive descriptor by hardware of receive descriptor. (R/W)

GDMA_INDSCR_BURST_EN_CHn Set this bit to 1 to enable INCR burst transfer for RX channel O reading descriptor when accessing internal RAM. (R/W)

GDMA_IN_DATA_BURST_EN_CHn Set this bit to 1 to enable INCR burst transfer for RX channel O receiving data when accessing internal RAM. (R/W)

GDMA_MEM_TRANS_EN_CHn Set this bit to 1 to enable automatic transmitting data from memory to memory via GDMA. (R/W)


Register 2.8. GDMA_IN_CONF1_CHn_REG (n: 0-2) (0x0074+192*n)

31 | (reserved) | 13 | 12 | 11 | 0
---|------------|-----|-----|----|---
0 | 0 | 0 | 0 | 0 | 0

GDMA_IN_CHECK_OWNER_CHn Set this bit to enable checking the owner attribute of the descriptor. (R/W)
```