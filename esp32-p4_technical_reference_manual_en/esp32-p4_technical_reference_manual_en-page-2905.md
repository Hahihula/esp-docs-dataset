

```markdown
Register 57.8. RMT_REF_CNT_RST_REG (0x00C8)
```

| bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | (reserved) | RMT_REF_CNT_RST_CH7 | RMT_REF_CNT_RST_CH6 | RMT_REF_CNT_RST_CH5 | RMT_REF_CNT_RST_CH4 | RMT_REF_CNT_RST_CH3 | RMT_REF_CNT_RST_CH2 | RMT_REF_CNT_RST_CH1 | RMT_REF_CNT_RST_CH0 |
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset |                |

RMT_REF_CNT_RST_Ch(n: 0-3) Configures whether to reset the clock divider of channel n.

O: No effect  
1: Reset  
(WT)

RMT_REF_CNT_RST_Ch(m: 4-7) Configures whether to reset the clock divider of channel m.

O: No effect  
1: Reset  
(WT)
```