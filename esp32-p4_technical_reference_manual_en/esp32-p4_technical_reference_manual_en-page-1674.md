

```markdown
Register 36.6. ISP_CCM_COEFO_REG (0x0014)

| 31 | 26 | 25 | ... | 13 | 12 | 0 |
|-----|----|----|-----|----|----|---|
| 0   | 0  | 0  | 0   | 4736 |     | Reset |

ISP_CCM_RR Configures the CCM RR parameter. The 12th bit is the sign bit, and bits [11:0] represent the absolute value. Bits [11:10] are the integer part, and bits [9:0] are the fractional part. (R/W)

ISP_CCM_RG Configures the CCM RG parameter, following the same bit structure and interpretation as ISP_CCM_RR. (R/W)


Register 36.7. ISP_CCM_COEF1_REG (0x0018)

| 31 | 26 | 25 | ... | 13 | 12 | 0 |
|-----|----|----|-----|----|----|---|
| 0   | 0  | 0  | 0   | 4416 |     | Reset |

ISP_CCM_RB Configures the CCM RB parameter, following the same bit structure and interpretation as ISP_CCM_RR. (R/W)

ISP_CCM_GR Configures the CCM GR parameter, following the same bit structure and interpretation as ISP_CCM_RR. (R/W)


Register 36.8. ISP_CCM_COEF3_REG (0x001C)

| 31 | 26 | 25 | ... | 13 | 12 | 0 |
|-----|----|----|-----|----|----|---|
| 0   | 0  | 0  | 0   | 4352 |     | Reset |

ISP_CCM_GG Configures the CCM GG parameter, following the same bit structure and interpretation as ISP_CCM_RR. (R/W)

ISP_CCM_GB Configures the CCM GB parameter, following the same bit structure and interpretation as ISP_CCM_RR. (R/W)
```