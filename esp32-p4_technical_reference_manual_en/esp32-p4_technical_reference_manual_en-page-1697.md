

```markdown
Register 36.46. ISP_AE_WINPIXNUM_REG (0x00D0)

| 31 | 17   | 16 | 0 |
|----:|------:|----:|---|
|    0 |      0 |     0 | Reset |

ISP_AE_SUBWIN_PIXNUM Configures the number of pixels in each sub-window. (R/W)

Register 36.47. ISP_AE_WIN_RECIPROCAL_REG (0x00D4)

| 31 | 20   | 19 | 0 |
|----:|------:|----:|---|
|    0 |      0 |     0 | Reset |

ISP_AE_SUBWIN_RECIP Configures the reciprocal of the number of pixels in each sub-window. It is a 20-bit fractional number, with [19:0] representing the fractional part. (R/W)

Register 36.48. ISP_SHARP_CTRL_REG (0x00F4)

| 31 | 24   | 23 | 16 | 15 | 8 | 7 | 0 |
|----:|------:|----:|----:|----:|---:|---:|---|
|    0 |      0 |     0 |     0 |     0 | Reset |

ISP_SHARP_THRESHOLD_LOW Configures the threshold for sharpening high-frequency details. Refer to section 36.5.2.10 for configuration. (R/W)

ISP_SHARP_THRESHOLD_HIGH Configures the threshold for sharpening high-frequency edges. Refer to section 36.5.2.10 for configuration. (R/W)

ISP_SHARP_AMOUNT_LOW Configures the gain for sharpening high-frequency details. Refer to section 36.5.2.10 for configuration. (R/W)

ISP_SHARP_AMOUNT_HIGH Configures the gain for sharpening high-frequency edges. Refer to section 36.5.2.10 for configuration. (R/W)
```