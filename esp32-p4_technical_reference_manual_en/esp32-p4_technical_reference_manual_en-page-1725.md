

```markdown
## Register 36.112. ISP_AE_BLOCK_MEAN_5_REG (0x00EC)

| 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|----|----|----|----|----|---|---|---|
|    | ISP_AE_B40_MEAN | ISP_AE_B41_MEAN | ISP_AE_B42_MEAN | ISP_AE_B43_MEAN | Reset |

- **ISP_AE_B43_MEAN** Represents the statistics from AE sub-window 43. (RO)
- **ISP_AE_B42_MEAN** Represents the statistics from AE sub-window 42. (RO)
- **ISP_AE_B41_MEAN** Represents the statistics from AE sub-window 41. (RO)
- **ISP_AE_B40_MEAN** Represents the statistics from AE sub-window 40. (RO)

## Register 36.113. ISP_AE_BLOCK_MEAN_6_REG (0x00FO)

| 31 | 24 | 23 | ... | 0 |
|----|----|----|-----|---|
|    | ISP_AE_B44_MEAN | (reserved) | Reset |

- **ISP_AE_B44_MEAN** Represents the statistics from AE sub-window 44. (RO)

## Register 36.114. ISP_AF_SUM_A_REG (0x014C)

| 31 | 30 | 29 | ... | 0 |
|----|----|----|-----|---|
|    | (reserved) | ISP_AF_SUMA | Reset |

- **ISP_AF_SUMA** Represents the sharpness statistics from AF window A. (RO)
```