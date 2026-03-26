

```markdown
## Register 39.36. H264_B_ROI_REGION7_REG (0x008C)

| 31 | 29 | 28 | 27 | 21 | 20 | 14 | 13 | 7 | 6 | Reset |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|----:|-------|
|   0 |   0 |   0 |    |    |    |    |    |    |    |       |

H264_B_ROI_REGION7_X Configures the horizontal start MBs of ROI 7 in video sequence B. (R/W)

H264_B_ROI_REGION7_Y Configures the vertical start MBs of ROI 7 in video sequence B. (R/W)

H264_B_ROI_REGION7_X_LEN Configures the number of MBs in horizontal direction of the ROI 7 in video sequence B. (R/W)

H264_B_ROI_REGION7_Y_LEN Configures the number of MBs in vertical direction of the ROI 7 in video sequence B. (R/W)

H264_B_ROI_REGION7_EN Configures whether to enable Video sequence B ROI 7.
0: Disable ROI
1: Enable ROI
(R/W)
```

```markdown
## Register 39.37. H264_B_ROI_REGIONO_3_QP_REG (0x0090)

| 31 | 28 | 27 | 21 | 20 | 14 | 13 | 7 | 6 | Reset |
|----:|----:|----:|----:|----:|----:|----:|----:|----:|-------|
|   0 |   0 |   0 |    |    |    |    |    |    |       |

H264_B_ROI_REGIONO_QP Configures H264 ROI 0 QP adjustment amount in video sequence B. (R/W)

H264_B_ROI_REGION1_QP Configures H264 ROI 1 QP adjustment amount in video sequence B. (R/W)

H264_B_ROI_REGION2_QP Configures H264 ROI 2 QP adjustment amount in video sequence B. (R/W)

H264_B_ROI_REGION3_QP Configures H264 ROI 3 QP adjustment amount in video sequence B. (R/W)
```