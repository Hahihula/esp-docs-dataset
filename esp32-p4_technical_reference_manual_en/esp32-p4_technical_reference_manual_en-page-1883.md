
```markdown
Register 39.25. H264_B_DECSCORE_OFFSET_REG (0x0060)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31-24     | (reserved)                                                                  |
| 23        | 0                                                                             |
| 22-18     | 0                                                                             |
| 17-12     | 0                                                                             |
| 11        | 0                                                                             |
| 10-6      | 0                                                                             |
| 5         | 0                                                                             |
| 4-0       | Reset                                                                         |

H264_B_I16x16_DECSCORE_OFFSET Configures video sequence B I16 x 16 MB decimate score offset. This offset will be added to i16 x 16 MB score. (R/W)

H264_B_I_CHROMA_DECSCORE_OFFSET Configures video sequence B I chroma MB decimate score offset. This offset will be added to I chroma MB score. (R/W)

H264_B_P16x16_DECSCORE_OFFSET Configures video sequence B p16 x 16 MB decimate score offset. This offset will be added to p16 x 16 MB score. (R/W)

H264_B_P_CHROMA_DECSCORE_OFFSET Configures video sequence B P chroma MB decimate score offset. This offset will be added to P chroma MB score. (R/W)


Register 39.26. H264_B_RC_CONFO_REG (0x0064)

| Bit Range | Description                                                                 |
|-----------|-----------------------------------------------------------------------------|
| 31        | (reserved)                                                                  |
| 23-22     | 0                                                                             |
| 21        | 0                                                                             |
| 20-17     | H264_B_MB_RATE_CTRL_EN                                                     |
| 16-15     | H264_B_RATE_CTRL_U                                                          |
| 14-9      | (reserved)                                                                  |
| 8         | H264_B_QP                                                                   |
| 7-0       | Reset                                                                        |

H264_B_QP Configures video sequence B frame level initial luma QP value. (R/W)

H264_B_RATE_CTRL_U Configures video sequence B parameter U value. U = int((float) u << 8). (R/W)

H264_B_MB_RATE_CTRL_EN Configures video sequence B whether to enable MB level rate control.
    0: Disable the MB level rate control
    1: Enable the MB level rate control
(R/W)
```