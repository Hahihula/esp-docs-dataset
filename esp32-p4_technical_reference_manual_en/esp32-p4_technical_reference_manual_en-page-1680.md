

```markdown
| 31 | 25 | 24 | 23 | (reserved) | ISP_DPC_TAIL_PIXEN_PULSE_TH | ISP_DPC_TAIL_PIXEN_PULSE_TL | ISP_DPC_MATRIX_CTRL_REG (0x0040) |
|-----|----:|----:|----:|------------:|-----------------------------:|------------------------------:|----------------------------------|
| 0   | 0  | 0  | 0  |             |                               |                                |                                    |
|     |    |    |    |            | 0x0                          | 0x0                           | Reset                             |

ISP_DPC_TAIL_PIXEN_PULSE_TL Configures the data control cycle for the tail-row data rate during pixel-to-matrix conversion in the DPC module. Within the ISP_DPC_TAIL_PIXEN_PULSE_TL clock cycles, only the first ISP_DPC_TAIL_PIXEN_PULSE_TH cycles are valid. Be cautious to configure this field, to prevent data processing from being deferred to the next frame.

This function is enabled only when both ISP_DPC_TAIL_PIXEN_PULSE_TL and ISP_DPC_TAIL_PIXEN_PULSE_TH are non-zero, and ISP_DPC_TAIL_PIXEN_PULSE_TH < ISP_DPC_TAIL_PIXEN_PULSE_TL. (R/W)

ISP_DPC_TAIL_PIXEN_PULSE_TH Configures the valid data cycle of the tail-row data rate during pixel-to-matrix conversion in the DPC module, which must be less than ISP_HADR_NUM - 1. (R/W)

ISP_DPC_PADDING_DATA Configures the padding data used for image edge expansion during pixel-to-matrix conversion in the DPC module. (R/W)

ISP_DPC_PADDING_MODE Configures the method of image edge expansion during pixel-to-matrix conversion in the DPC module.
0: Automatically padded with pixel values from the image edge
1: Padded with the data in ISP_DPC_PADDING_DATA
(R/W)
```