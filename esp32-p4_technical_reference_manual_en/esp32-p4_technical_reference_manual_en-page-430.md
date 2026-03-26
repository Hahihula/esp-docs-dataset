

```markdown
Register 6.5. DMA2D_OUT_ARB_CHn_REG (n: 0-3) (0x003C+0x100*n)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset (0x0) | 0x1 | 0x1 |    |    |    |
```

DMA2D_OUT_ARB_TOKEN_NUM_CHn Configures the weight (i.e the number of tokens) of TX channel n.
Value range: 0 ~ 15. (R/W)

DMA2D_OUT_ARB_PRIORITY_CHn Configures the lower two bits of TX channel n priority.
Together with DMA2D_OUT_ARB_PRIORITY_H_CHn, this field forms a 4-bit priority value for TX channel n, ranging from 0 (lowest) to 15 (highest). (R/W)

DMA2D_OUT_ARB_PRIORITY_H_CHn Configures the higher two bits of TX channel n priority.
Together with DMA2D_OUT_ARB_PRIORITY_CHn, this field forms a 4-bit priority value for TX channel n, ranging from 0 (lowest) to 15 (highest). (R/W)
```