

```markdown
Register 35.4. JPEG_EXTD_CONFIG_REG (0x000C)

| Bit 31 | ... | 2 | 1 | 0 |
|--------|-----|---|---|---|
|        |     |   |   | Reset |

JPEG_EXTD_COLOR_SPACE_EN Configure whether to enable extended color space conversion options.
O: Disable
1: Enable (R/W)

JPEG_EXTD_COLOR_SPACE Configure the extended color space format to be converted. Valid when JPEG_EXTD_COLOR_SPACE_EN configured to 1.
O: YUV444
1: YUV420 (R/W)


Register 35.5. JPEG_TOQNR_REG (0x0010)

| Bit 31 | ... | 0 |
|--------|-----|---|
|        |     | Reset |

JPEG_TO_QNR_VAL Configures the quantization coefficients of the quantization table 0 in FIFO mode. (HRO)


Register 35.6. JPEG_T1QNR_REG (0x0014)

| Bit 31 | ... | 0 |
|--------|-----|---|
|        |     | Reset |

JPEG_T1_QNR_VAL Configures the quantization coefficients of the quantization table 1 in FIFO mode. (HRO)
```