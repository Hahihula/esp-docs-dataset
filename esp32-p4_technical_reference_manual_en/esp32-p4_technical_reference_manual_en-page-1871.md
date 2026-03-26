

```markdown
Register 39.8. H264_A_RC_CONF1_REG (0x001C)

| 31 | 30 | 19 | 18 | 13 | 12 | 7 | 6 | 3 | 2 | 0 |
|-----|----:|----:|----:|----:|----:|---:|---:|---:|---:|---|
| 0   |    0|     |     |     |     |   0|   0|   0|   0|Reset|

H264_A_CHROMA_DC_QP_DELTA Configures video sequence A chroma DC QP offset based on Chroma QP. Chroma DC QP = Chroma QP(after map) + reg_chroma_dc_QP_delta. (R/W)

H264_A_CHROMA_QP_DELTA Configures video sequence A chroma QP offset based on luma QP. Chroma QP(before map) = Luma QP + reg_chroma_qp_delta. (R/W)

H264_A_QP_MIN Configures video sequence A allowed luma QP min value. (R/W)

H264_A_QP_MAX Configures video sequence A allowed luma QP max value. (R/W)

H264_A_MAD_FRAME_PRED Configures video sequence A frame level predicted MB MAD value. (R/W)
```

```markdown
Register 39.9. H264_A_DB_BYPASS_REG (0x0020)

| 31 | ... | 1 | 0 |
|----|-----|---|---|
|    |     |   |Reset|

H264_A_BYPASS_DB_FILTER Configures whether to bypass video sequence A deblocking filter.
0: Do not bypass the deblocking filter
1: Bypass the deblocking filter
(R/W)
```