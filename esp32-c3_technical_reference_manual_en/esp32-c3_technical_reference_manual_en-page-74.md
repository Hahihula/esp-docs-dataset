

```markdown
Register 21. GDMA_INT_RAW_CHn_REG (n: 0-2) (0x0000+16*n)
```

Continued from the previous page...

GDMA_IN_DSCR_EMPTY_CHn_INT_RAW The raw interrupt bit turns to high level when RX buffer pointed by inlink is full and receiving data is not completed, but there is no more inlink for RX channel 0. (R/WTC/SS)

GDMA_OUT_TOTAL_EOF_CHn_INT_RAW The raw interrupt bit turns to high level when data corresponding a outlink (includes one descriptor or few descriptors) is transmitted out for TX channel 0. (R/WTC/SS)

GDMA_INFIFO_OVF_CHn_INT_RAW This raw interrupt bit turns to high level when level 1 FIFO of RX channel 0 is overflow. (R/WTC/SS)

GDMA_INFIFO_UDF_CHn_INT_RAW This raw interrupt bit turns to high level when level 1 FIFO of RX channel 0 is underflow. (R/WTC/SS)

GDMA_OUTFIFO_OVF_CHn_INT_RAW This raw interrupt bit turns to high level when level 1 FIFO of TX channel 0 is overflow. (R/WTC/SS)

GDMA_OUTFIFO_UDF_CHn_INT_RAW This raw interrupt bit turns to high level when level 1 FIFO of TX channel 0 is underflow. (R/WTC/SS)
```