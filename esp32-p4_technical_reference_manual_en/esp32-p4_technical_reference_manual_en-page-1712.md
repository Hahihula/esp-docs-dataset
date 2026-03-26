

```markdown
Register 36.77. ISP_HIST_MODE_REG (0x01A4)

ISP_HIST_MODE   Configures the HIST sampling mode.
0: RAW_B
1: RAW_GB
2: RAW_GR
3: RAW_R
4: RGB
5: YUV_Y
6: YUV_U
7: YUV_V

(R/W)
```

```markdown
Register 36.78. ISP_HIST_COEFF_REG (0x01A8)

ISP_HIST_COEFF_B   Configures the B weight for RGB to brightness conversion when HIST statistics mode set to RGB. Bits [7:0] are the fractional part. (R/W)

ISP_HIST_COEFF_G   Configures the G weight for RGB to brightness conversion when HIST statistics mode set to RGB. Bits [7:0] are the fractional part. (R/W)

ISP_HIST_COEFF_R   Configures the R weight for RGB to brightness conversion when HIST statistics mode set to RGB. Bits [7:0] are the fractional part. (R/W)
```