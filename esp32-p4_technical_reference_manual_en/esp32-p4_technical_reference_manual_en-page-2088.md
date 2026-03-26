

```markdown
Register 40.18. CSI_HOST_INT_ST_PHY_REG (0x0110)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | CSI_HOST_ST_PHY_ERRSOTH_1 | CSI_HOST_ST_PHY_ERRRESO_0 | (reserved) | (reserved) | Reset |
```

CSI_HOST_ST_PHY_ERRSOTHS_n (n: 0-1) Represents whether the PHY_ERRSOTHS_n error occurs.

0: Do not occur
1: Occur
(RC)

CSI_HOST_ST_PHY_ERRRESC_n (n: 0-1) Represents whether the PHY_ERRRESC_n error occurs.

0: Do not occur
1: Occur
(RC)
```