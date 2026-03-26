

```markdown
Register 36.21. ISP_DEMOSAIC_MATRIX_CTRL_REG (0x0058)

| Bit Range | Field Name                                 | Description                                                                 |
|-----------|---------------------------------------------|-----------------------------------------------------------------------------|
| 31-24     | (reserved)                                 |                                                                             |
| 23        | ISP_DEMOSAIC_PADDING_MODE                  | Configures the method of image edge expansion during pixel-to-matrix conversion in the demosaic module. <br>0: Automatically padded with pixel values from the image edge <br>1: Padded with the data in `ISP_DEMOSAIC_PADDING_DATA` (R/W) |
| 22-16     | ISP_DEMOSAIC_PADDING_DATA                  | Configures the padding data used during image edge expansion in pixel-to-matrix conversion of the demosaic module. (R/W) |
| 15        | ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TH           | Configures the valid data cycle of the tail-row data rate during pixel-to-matrix conversion in the demosaic module, which must be less than `ISP_HADR_NUM` - 1. (R/W) |
| 14-8      | ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TH           | Configures the valid data cycle of the tail-row data rate during pixel-to-matrix conversion in the demosaic module, which must be less than `ISP_HADR_NUM` - 1. (R/W) |
| 7-0       | ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TL           | Configures the data control cycle for the tail-row data rate during pixel-to-matrix conversion in the demosaic module. Within `ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TL` clock cycles, only the first `ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TH` cycles are valid. Be cautious to configure this field, to prevent data processing from being deferred to the next frame. This feature is enabled only when both `ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TL` and `ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TH` are non-zero, and `ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TH < ISP_DEMOSAIC_TAIL_PIXEN_PULSE_TL`. (R/W) |
```