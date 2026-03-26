

```markdown
Register 39.13. H264_A_ROI_REGION3_REG (0x0030)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 30  | H264_A_ROI_REGION3_EN          | Configures whether to enable Video sequence A ROI 3.                         |
|     |                                 | 0: Disable ROI                                                              |
|     |                                 | 1: Enable ROI                                                               |
| 29  |                                | (reserved)                                                                  |
| 28  | H264_A_ROI_REGION3_X           | Configures the horizontal start MBs of ROI 3 in Video sequence A. (R/W)      |
| 27  |                                 |                                                                             |
| 21  | H264_A_ROI_REGION3_Y           | Configures the vertical start MBs of ROI 3 in Video sequence A. (R/W)        |
| 20  |                                 |                                                                             |
| 14  | H264_A_ROI_REGION3_X_LEN       | Configures the number of MBs in horizontal direction of the ROI 3 in video sequence A. (R/W) |
| 13  |                                 |                                                                             |
| 7   | H264_A_ROI_REGION3_Y_LEN       | Configures the number of MBs in vertical direction of the ROI 3 in video sequence A. (R/W) |
| 6   |                                 |                                                                             |
| 0   | Reset                          |                                                                             |

H264_A_ROI_REGION3_X Configures the horizontal start MBs of ROI 3 in Video sequence A. (R/W)

H264_A_ROI_REGION3_Y Configures the vertical start MBs of ROI 3 in Video sequence A. (R/W)

H264_A_ROI_REGION3_X_LEN Configures the number of MBs in horizontal direction of the ROI 3 in video sequence A. (R/W)

H264_A_ROI_REGION3_Y_LEN Configures the number of MBs in vertical direction of the ROI 3 in video sequence A. (R/W)

H264_A_ROI_REGION3_EN Configures whether to enable Video sequence A ROI 3.
0: Disable ROI
1: Enable ROI
(R/W)
```