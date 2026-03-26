

```markdown
Register 36.52. ISP_SHARP_MATRIX_CTRL_REG (0x0104)

| 31 | 25 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----|----:|----:|----:|----:|----:|---:|---:|---|
| 0   | 0 0 | 0 0 | 0  | 0  | 0x0| 0x0| Reset |

ISP_SHARP_TAIL_PIXEN_PULSE_TL Configures the data control cycle for the tail-row data rate during pixel-to-matrix conversion in the sharpen module.
Within ISP_SHARP_TAIL_PIXEN_PULSE_TL clock cycles, only the first ISP_SHARP_TAIL_PIXEN_PULSE_TH cycles are valid. Be cautious to configure this field, to prevent data processing from being deferred to the next frame.
This feature is enabled only when both ISP_SHARP_TAIL_PIXEN_PULSE_TL and ISP_SHARP_TAIL_PIXEN_PULSE_TH are non-zero, and ISP_SHARP_TAIL_PIXEN_PULSE_TH < ISP_SHARP_TAIL_PIXEN_PULSE_TL. (R/W)

ISP_SHARP_TAIL_PIXEN_PULSE_TH Configures the valid data cycle of the tail-row data rate during pixel-to-matrix conversion in the sharpen module, which must be less than ISP_HADR_NUM - 1. (R/W)

ISP_SHARP_PADDING_DATA Configures the padding data used during image edge expansion in pixel-to-matrix conversion of the sharpen module. (R/W)

ISP_SHARP_PADDING_MODE Configures the method of image edge expansion during pixel-to-matrix conversion in the sharpen module.
0: Automatically padded with pixel values from the image edge
1: Padded with the data in ISP_SHARP_PADDING_DATA
(R/W)
```

Register 36.53. ISP_SHARP_CTRL1_REG (0x0108)

| 31 | ... | 7 | 0 |
|-----|------|---:|---|
| 0   | 0x0 | Reset |

ISP_SHARP_GRADIENT_MAX Represents the maximum pixel value of high-frequency components in the sharpen module, automatically refreshed every frame. (RO)
```