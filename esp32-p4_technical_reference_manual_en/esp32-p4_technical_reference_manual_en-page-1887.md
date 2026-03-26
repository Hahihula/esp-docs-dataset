

```markdown
| Chapter 39 H264 Encoder                                                                 GoBack |
|------------------------------------------------------------------------------------------|
| Register 39.31. H264_B_ROI_REGION2_REG (0x0078)                                           |
|                                                                                        |
| +--------+--------+--------+--------+--------+--------+--------+--------+--------+--------+
| |31      |30      |29      |28      |27      |21      |20      |14      |7       |0       |
| +--------+--------+--------+--------+--------+--------+--------+--------+--------+--------+
| (reserved)|H264_B_ROI_REGION2_EN|H264_B_ROI_REGION2_Y_LEN|H264_B_ROI_REGION2_X_LEN|Reset    |
| 0        |0          |0        |0        |0       |0       |0       |0       |0       |        |

H264_B_ROI_REGION2_X Configures the horizontal start MBs of ROI 2 in Video sequence B. (R/W)

H264_B_ROI_REGION2_Y Configures the vertical start MBs of ROI 2 in Video sequence B. (R/W)

H264_B_ROI_REGION2_X_LEN Configures the number of MBs in horizontal direction of the ROI 2
in Video sequence B. (R/W)

H264_B_ROI_REGION2_Y_LEN Configures the number of MBs in vertical direction of the ROI 2 in
Video sequence B. (R/W)

H264_B_ROI_REGION2_EN Configures whether to enable Video sequence B ROI 2.
0: Disable ROI
1: Enable ROI
(R/W)
```