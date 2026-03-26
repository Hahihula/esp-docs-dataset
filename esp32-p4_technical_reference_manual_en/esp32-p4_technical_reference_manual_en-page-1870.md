

```markdown
Register 39.6. H264_A_DECSCORE_OFFSET_REG (0x0014)

| Bit Range | Field Description                  |
|-----------|------------------------------------|
| 31-24     | (reserved)                        |
| 23        | O                                 |
| 18-17     |                                    |
| 12-11     | O                                 |
| 6-5       | O                                 |
| 0         | Reset                             |

H264_A_I16x16_DECSCORE_OFFSET Configures video sequence A i16x16 MB decimate score offset. This offset will be added to i16x16 MB score. (R/W)

H264_A_I_CHROMA_DECSCORE_OFFSET Configures video sequence A I chroma MB decimate score offset. This offset will be added to I chroma MB score. (R/W)

H264_A_P16x16_DECSCORE_OFFSET Configures video sequence A p16x16 MB decimate score offset. This offset will be added to p16x16 MB score. (R/W)

H264_A_P_CHROMA_DECSCORE_OFFSET Configures video sequence A P chroma MB decimate score offset. This offset will be added to P chroma MB score. (R/W)


Register 39.7. H264_A_RC_CONFO_REG (0x0018)

| Bit Range | Field Description                  |
|-----------|------------------------------------|
| 31        | (reserved)                        |
| 23-22     | O                                 |
| 21        | O                                 |
|           |                                    |
|           | O                                 |
| 6-5       | O                                 |
| 0         | Reset                             |

H264_A_QP Configures video sequence A frame level initial luma QP value. (R/W)

H264_A_RATE_CTRL_U Configures video sequence A parameter U value. U = int((float) u << 8). (R/W)

H264_A_MB_RATE_CTRL_EN Configures video sequence A whether to enable the MB level rate control.
    0: Disable the MB level rate control
    1: Enable the MB level rate control
(R/W)
```