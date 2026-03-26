

```markdown
Register 36.16. ISP_DPC_CONF_REG (0x003C)

| 31 | 28 | 27 | 22 | 21 | 16 | 15 | 8 | 7 | 0 |
|-----|----|----|----|----|----|----|---|---|---|
| 0   | 0  | 0  |    |    |    |    |    |    | Reset |

ISP_DPC_THRESHOLD_L Configures the defective pixel threshold for black image static calibration, or the low threshold in dynamic correction Algorithm 0 (8-bit valid), or the low threshold in dynamic correction Algorithm 1 (5-bit valid, maximum value is 16). For details, refer to Section 36.5.2.2. (R/W)

ISP_DPC_THRESHOLD_H Configures the defective pixel threshold for white image static calibration, or the high threshold in dynamic correction Algorithm 0 (8-bit valid), or the high threshold in dynamic correction Algorithm 1 (5-bit valid, maximum value is 16). For details, refer to Section 36.5.2.2. (R/W)

ISP_DPC_FACTOR_DARK Configures the dark pixel factor used in dynamic correction Algorithm 1. (R/W)

ISP_DPC_FACTOR_BRIG Configures the bright pixel factor used in dynamic correction Algorithm 1. (R/W)
```