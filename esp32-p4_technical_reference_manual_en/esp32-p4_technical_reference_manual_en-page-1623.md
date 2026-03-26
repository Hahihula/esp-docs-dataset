

```markdown
Register 35.10. JPEG_CO_REG (0x0024)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved(0)                                                                |
| 24  | JPEG_CO_ID Configures the ID of component0 in decoder mode. (R/W)           |
| 23  |                                                                     |
| 16  | JPEG_CO_X_FACTOR Configures the horizontal sampling factor of component0 in decoder mode. (R/W) |
| 15  |                                                                     |
| 12  | JPEG_CO_Y_FACTOR Configures the vertical sampling factor of component0 in decoder mode. (R/W) |
| 11  |                                                                     |
| 8   |                                                                     |
| 7   |                                                                     |
| 6-0 | JPEG_CO_DQT_TBL_SEL Configures the selected quantization coefficient table ID for component0 in decoder mode. (R/W) |

JPEG_CO_DQT_TBL_SEL Configures the selected quantization coefficient table ID for component0 in decoder mode. (R/W)

JPEG_CO_Y_FACTOR Configures the vertical sampling factor of component0 in decoder mode. (R/W)

JPEG_CO_X_FACTOR Configures the horizontal sampling factor of component0 in decoder mode. (R/W)

JPEG_CO_ID Configures the ID of component0 in decoder mode. (R/W)
```

```markdown
Register 35.11. JPEG_C1_REG (0x0028)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | reserved(0)                                                                |
| 24  | JPEG_C1_ID Configures the ID of component1 in decoder mode. (R/W)           |
| 23  |                                                                     |
| 16  | JPEG_C1_X_FACTOR Configures the horizontal sampling factor of component1 in decoder mode. (R/W) |
| 15  |                                                                     |
| 12  | JPEG_C1_Y_FACTOR Configures the vertical sampling factor of component1 in decoder mode. (R/W) |
| 11  |                                                                     |
| 8   |                                                                     |
| 7   |                                                                     |
| 6-0 | JPEG_C1_DQT_TBL_SEL Configures the selected quantization coefficient table ID for component1 in decoder mode. (R/W) |

JPEG_C1_DQT_TBL_SEL Configures the selected quantization coefficient table ID for component1 in decoder mode. (R/W)

JPEG_C1_Y_FACTOR Configures the vertical sampling factor of component1 in decoder mode. (R/W)

JPEG_C1_X_FACTOR Configures the horizontal sampling factor of component1 in decoder mode. (R/W)

JPEG_C1_ID Configures the ID of component1 in decoder mode. (R/W)
```