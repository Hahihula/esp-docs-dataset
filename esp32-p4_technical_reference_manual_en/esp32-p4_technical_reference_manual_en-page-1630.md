

```markdown
Register 35.17: JPEG_INT_ST_REG (0x0040)

Continued from the previous page...

| Field Name                                 | Description                                                                 | Masked? | Interrupt Status of |
|--------------------------------------------|-----------------------------------------------------------------------------|---------|---------------------|
| JPEG_EN_FRAME_EOF_ERR_INT_ST               | The JPEG_EN_FRAME_EOF_ERR_INT. (RO)                                         | masked  | interrupt           |
| JPEG_EN_FRAME_EOF_LACK_INT_ST              | The JPEG_EN_FRAME_EOF_LACK_INT. (RO)                                        | masked  | interrupt           |
| JPEG_DE_FRAME_EOF_ERR_INT_ST               | The JPEG_DE_FRAME_EOF_ERR_INT. (RO)                                         | masked  | interrupt           |
| JPEG_DE_FRAME_EOF_LACK_INT_ST              | The JPEG_DE_FRAME_EOF_LACK_INT. (RO)                                        | masked  | interrupt           |
| JPEG_SOS_UNMATCH_ERR_INT_ST                | The JPEG_SOS_UNMATCH_ERR_INT. (RO)                                          | masked  | interrupt           |
| JPEG_MARKER_ERR_FST_SCAN_INT_ST            | The JPEG_MARKER_ERR_FST_SCAN_INT. (RO)                                      | masked  | interrupt           |
| JPEG_MARKER_ERR_OTHER_SCAN_INT_ST          | The JPEG_MARKER_ERR_OTHER_SCAN_INT. (RO)                                    | masked  | interrupt           |
| JPEG_UNDET_INT_ST                          | The masked interrupt status of JPEG_UNDET_INT. (RO)                         |         |                     |
| JPEG_DECODE_TIMEOUT_INT_ST                 | The masked interrupt status of JPEG_DECODE_TIMEOUT_INT. (RO)                |         |                     |
```