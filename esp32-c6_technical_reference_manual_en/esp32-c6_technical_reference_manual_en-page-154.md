

```markdown
Register 4.12. GDMA_IN_CONF1_CHn_REG (n: 0-2) (0x0074+0xC0*n)

GDMA_IN_CHECK_OWNER_CHn Configures whether or not to enable owner bit check for RX channel n.
O: Disable
1: Enable
(R/W)
```

```markdown
Register 4.13. GDMA_IN_POP_CHn_REG (n: 0-2) (0x007C+0xC0*n)

GDMA_INFIFO_RDATA_CHn Represents the data popped from GDMA FIFO. (RO)

GDMA_INFIFO_POP_CHn Configures whether or not to pop data from GDMA FIFO.
O: Invalid. No effect
1: Pop
(WT)
```