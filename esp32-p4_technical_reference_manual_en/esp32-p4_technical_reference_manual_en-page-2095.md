

```markdown
Register 40.30. CSI_HOST_INT_ST_PLD_CRC_FATAL_REG (0x02B0)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset | CSI_HOST_ST_ERR_CRC_VC15 | CSI_HOST_ST_ERR_CRC_VC14 | ... | CSI_HOST_ST_ERR_CRC_VC0 |
|(reserved)| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

CSI_HOST_ST_ERR_CRC_VCn (n: 0-15) Represents whether the ERR_CRC_VCn error occurs.
0: Do not occur
1: Occur
(RC)

Register 40.31. CSI_HOST_INT_MSK_PLD_CRC_FATAL_REG (0x02B4)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    |    |    |    | Reset | CSI_HOST_MASK_ERR_CRC_VC15 | ... | CSI_HOST_MASK_ERR_CRC_VC0 |
|(reserved)| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

CSI_HOST_MASK_ERR_CRC_VCn (n: 0-15) Configures whether to mask CSI_HOST_ST_ERR_CRC_VCn.
0: Mask the error interrupt
1: Enable the error interrupt
(R/W)
```