
```markdown
Register 40.34. CSI_HOST_INT_MSK_DATA_ID_REG (0x02C4)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | Reset | reserved |
| 15  | CSI_HOST_MASK_ERR_ID_VC15 |
| 14  | CSI_HOST_MASK_ERR_ID_VC14 |
| 13  | CSI_HOST_MASK_ERR_ID_VC13 |
| 12  | CSI_HOST_MASK_ERR_ID_VC12 |
| 11  | CSI_HOST_MASK_ERR_ID_VC11 |
| 10  | CSI_HOST_MASK_ERR_ID_VC10 |
| 9   | CSI_HOST_MASK_ERR_ID_VC9  |
| 8   | CSI_HOST_MASK_ERR_ID_VC8  |
| 7   | CSI_HOST_MASK_ERR_ID_VC7  |
| 6   | CSI_HOST_MASK_ERR_ID_VC6  |
| 5   | CSI_HOST_MASK_ERR_ID_VC5  |
| 4   | CSI_HOST_MASK_ERR_ID_VC4  |
| 3   | CSI_HOST_MASK_ERR_ID_VC3  |
| 2   | CSI_HOST_MASK_ERR_ID_VC2  |
| 1   | CSI_HOST_MASK_ERR_ID_VC1  |
| 0   | Reset                     |

CSI_HOST_MASK_ERR_ID_VCn (n: 0-15) Configures whether to mask CSI_HOST_ST_ERR_ID_VCn.
O: Mask the error interrupt
1: Enable the error interrupt
(R/W)
```


```markdown
Register 40.35. CSI_HOST_INT_FORCE_DATA_ID_REG (0x02C8)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |    |    | Reset | reserved |
| 15  | CSI_HOST_FORCE_ERR_ID_VC15 |
| 14  | CSI_HOST_FORCE_ERR_ID_VC14 |
| 13  | CSI_HOST_FORCE_ERR_ID_VC13 |
| 12  | CSI_HOST_FORCE_ERR_ID_VC12 |
| 11  | CSI_HOST_FORCE_ERR_ID_VC11 |
| 10  | CSI_HOST_FORCE_ERR_ID_VC10 |
| 9   | CSI_HOST_FORCE_ERR_ID_VC9  |
| 8   | CSI_HOST_FORCE_ERR_ID_VC8  |
| 7   | CSI_HOST_FORCE_ERR_ID_VC7  |
| 6   | CSI_HOST_FORCE_ERR_ID_VC6  |
| 5   | CSI_HOST_FORCE_ERR_ID_VC5  |
| 4   | CSI_HOST_FORCE_ERR_ID_VC4  |
| 3   | CSI_HOST_FORCE_ERR_ID_VC3  |
| 2   | CSI_HOST_FORCE_ERR_ID_VC2  |
| 1   | CSI_HOST_FORCE_ERR_ID_VC1  |
| 0   | Reset                     |

CSI_HOST_FORCE_ERR_ID_VCn (n: 0-15) Configures whether to force set CSI_HOST_ST_ERR_ID_VCn to 1.
O: Do not force set
1: Force set
(R/W)
```