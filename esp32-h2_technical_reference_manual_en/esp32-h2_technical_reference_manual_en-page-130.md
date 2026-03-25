

```markdown
Register 3.16. GDMA_OUT_CONF1_CHn_REG (n: 0-2) (0x00D4+0xC0*n)

GDMA_OUT_CHECK_OWNER_CHn Configures whether or not to enable owner bit check for TX channel n.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 3.17. GDMA_OUT_PUSH_CHn_REG (n: 0-2) (0x00DC+0xC0*n)

GDMA_OUTFIFO_WDATA_CHn Represents the data that need to be pushed into GDMA FIFO. (R/W)
GDMA_OUTFIFO_PUSH_CHn Configures whether to push data into GDMA FIFO.
O: Invalid. No effect
1: Push
(WT)
```