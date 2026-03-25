

```markdown
Register 3.11. GDMA_IN_CONFO_CHn_REG (n: 0-2) (0x0070+0xC0*n)

GDMA_IN_RST_CHn   Write 1 and then 0 to reset GDMA channel 0 RX FSM and RX FIFO pointer.(R/W)

GDMA_IN_LOOP_TEST_CHn   Reserved. (R/W)

GDMA_INDSR_BURST_EN_CHn   Configures whether or not to enable INCR burst transfer for RX channel n to read descriptors.
    0: Disable
    1: Enable
    (R/W)

GDMA_IN_DATA_BURST_EN_CHn   Configures whether or not to enable INCR burst transfer for RX channel n.
    0: Disable
    1: Enable
    (R/W)

GDMA_MEM_TRAN_EN_CHn   Configures whether or not to enable memory-to-memory data transfer.
    0: Disable
    1: Enable
    (R/W)

GDMA_IN_ETM_EN_CHn   Configures whether or not to enable ETM control for RX channel n.
    0: Disable
    1: Enable
    (R/W)
```