

```markdown
Register 39.27. H264_B_RC_CONF1_REG (0x0068)

| (reserved) | H264_B_MAD_FRAME_PRED | H264_B_QP_MAX | H264_B_QP_MIN | H264_B_CHROMA_QP_DELTA | H264_B_CHROMA_DC_QP_DELTA |
|:-----------:|:---------------------:|:-------------:|:-------------:|:-----------------------:|:--------------------------|
|     31      |           19          |       18      |       13      |         7               |        6                  |
|             |                       |               |               |                        |                          |
|   0         |           0           |       0       |       0       |           0             |           0               |

H264_B_CHROMA_DC_QP_DELTA Configures video sequence B chroma DC QP offset based on Chroma QP. Chroma DC QP = Chroma QP(after ping) + reg_chroma_dc_qp_delta. (R/W)

H264_B_CHROMA_QP_DELTA Configures video sequence B chroma QP offset based on luma QP. Chroma QP(before mapping) = Luma QP + reg_chroma_qp_delta. (R/W)

H264_B_QP_MIN Configures the minimum allowed luma QP value for video sequence B. (R/W)

H264_B_QP_MAX Configures the maximum allowed luma QP value for video sequence B. (R/W)

H264_B_MAD_FRAME_PRED Configures the MAD value for frame-level predicted MB in video sequence B. (R/W)


Register 39.28. H264_B_DB_BYPASS_REG (0x006C)

| (reserved) | H264_B_BYPASS_DB_FILTER |
|:-----------:|:-----------------------|
|     31      |           1            |
|             |           0            |

H264_B_BYPASS_DB_FILTER Configures whether to bypass video sequence B deblocking filter.
0: Not bypass the deblocking filter
1: Bypass the deblocking filter
(R/W)
```