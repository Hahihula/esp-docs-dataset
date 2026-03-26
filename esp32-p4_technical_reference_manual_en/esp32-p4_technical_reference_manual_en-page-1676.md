

```markdown
Register 36.11. ISP_BF_MATRIX_CTRL_REG (0x0028)

| 31 | 25 | 24 | 23 | 22 | 21 | 20 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | ISP_BF_PADDING_MODE | ISP_BF_PADDING_DATA | ISP_BF_TAIL_PIXEN_PULSE_TH | ISP_BF_TAIL_PIXEN_PULSE_TL |
| 0   | 0   | 0   | 0   | 0x0 |     |     | 0x0 |     | Reset |

ISP_BF_TAIL_PIXEN_PULSE_TL Configures the data control cycle for the tail-row data rate during pixel-to-matrix conversion in the BF module.
Within ISP_BF_TAIL_PIXEN_PULSE_TL clock cycles, only the first ISP_BF_TAIL_PIXEN_PULSE_TH cycles are valid. Be cautious to configure this field, to prevent data processing from being deferred to the next frame.

This feature is enabled only when both ISP_BF_TAIL_PIXEN_PULSE_TL and ISP_BF_TAIL_PIXEN_PULSE_TH are non-zero, and ISP_BF_TAIL_PIXEN_PULSE_TH < ISP_BF_TAIL_PIXEN_PULSE_TL. (R/W)

ISP_BF_TAIL_PIXEN_PULSE_TH Configures the valid data cycle of the tail-row data rate during pixel-to-matrix conversion in the BF module, which must be less than ISP_HADR_NUM - 1. (R/W)

ISP_BF_PADDING_DATA Configures the padding data used during image edge expansion in pixel-to-matrix conversion of the BF module. (R/W)

ISP_BF_PADDING_MODE Configures the method of image edge expansion during pixel-to-matrix conversion in the BF module.
0: Automatically padded with pixel values from the image edge
1: Padded with the data in ISP_BF_PADDING_DATA
(R/W)
```

```markdown
Register 36.12. ISP_BF_SIGMA_REG (0x002C)

| 31 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | (reserved) | ISP_SIGMA |
| 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 0   | 2   | Reset |

ISP_SIGMA Configures the strength of noise reduction in the BF module. Values from 2 to 20 represent increasing strength, while other values indicate maximum strength. (R/W)
```