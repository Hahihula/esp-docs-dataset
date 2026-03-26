

```markdown
Register 35.12. JPEG_C2_REG (0x002C)

| 31 | reserved(1) | 24 | 23 | 16 | 15 | JPEG_C2_ID | 12 | 11 | JPEG_C2_X_FACTOR | 8 | 7 | JPEG_C2_Y_FACTOR | 0 |
|-----|-------------|-----|-----|-----|-----|------------|-----|-----|------------------|---|---|------------------|---|
|     |             |     |     |     |     |            |     |     |                  |   |   |                  |   |
| 0   | 0   0   0   0   0 |     | O   |     | 1   |     | 1   |     | O   | Reset |

JPEG_C2_DQT_TBL_SEL Configures the selected quantization coefficient table ID for component2 in decoder mode. (R/W)

JPEG_C2_Y_FACTOR Configures the vertical sampling factor of component2 in decoder mode. (R/W)

JPEG_C2_X_FACTOR Configures the horizontal sampling factor of component2 in decoder mode. (R/W)

JPEG_C2_ID Configures the ID of component2 in decoder mode. (R/W)


Register 35.13. JPEG_C3_REG (0x0030)

| 31 | reserved(1) | 24 | 23 | 16 | 15 | JPEG_C3_ID | 12 | 11 | JPEG_C3_X_FACTOR | 8 | 7 | JPEG_C3_Y_FACTOR | 0 |
|-----|-------------|-----|-----|-----|-----|------------|-----|-----|------------------|---|---|------------------|---|
|     |             |     |     |     |     |            |     |     |                  |   |   |                  |   |
| 0   | 0   0   0   0   0 |     | O   |     | 1   |     | 1   |     | O   | Reset |

JPEG_C3_DQT_TBL_SEL Configures the selected quantization coefficient table ID for component3 in decoder mode. (R/W)

JPEG_C3_Y_FACTOR Configures the vertical sampling factor of component3 in decoder mode. (R/W)

JPEG_C3_X_FACTOR Configures the horizontal sampling factor of component3 in decoder mode. (R/W)

JPEG_C3_ID Configures the ID of component3 in decoder mode. (R/W)
```