

```markdown
Register 36.71. ISP_AWB_TH_LUM_REG (0x0170)

| 31 | 26 | 25 |        | 16 | 15 | 10 | 9 |         |
|----:|----:|----:|--------|----:|----:|----:|---:|---------|
|    |    |    | (reserved) | ISP_AWB_MAX_LUM | 0 | 0 | 0 | 0 | Reset |

ISP_AWB_MIN_LUM Configures the lower limit of R+G+B luminance for AWB white patch filtering. (R/W)
ISP_AWB_MAX_LUM Configures the upper limit of R+G+B luminance for AWB white patch filtering. (R/W)

Register 36.72. ISP_AWB_TH_RG_REG (0x0174)

| 31 | 26 | 25 |        | 16 | 15 | 10 | 9 |         |
|----:|----:|----:|--------|----:|----:|----:|---:|---------|
|    |    |    | (reserved) | ISP_AWB_MAX_RG | 0x3ff | 0 | 0 | 0 | Reset |

ISP_AWB_MIN_RG Configures the lower limit of R/G ratio for AWB white point filtering. Bits [9:8] are the integer part, and bits [7:0] are the fractional part. (R/W)
ISP_AWB_MAX_RG Configures the upper limit of R/G ratio for AWB white point filtering. Bits [9:8] are the integer part, and bits [7:0] are the fractional part. (R/W)

Register 36.73. ISP_AWB_TH_BG_REG (0x0178)
```