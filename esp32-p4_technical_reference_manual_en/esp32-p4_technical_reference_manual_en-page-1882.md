

```markdown
Register 39.23. H264_B_SYS_CONF_REG (0x0058)

| 31 | 30     | 29           | 14   | 13             | 7       | 6                  | 3                   |
|-----|--------|--------------|------|----------------|---------|--------------------|---------------------|
| 0   | 0      |              |      |                |         |                    |                     |

H264_B_DB_TMP_READY_TRIGGER_MB_NUM Configures when to trigger video sequence B H264_DB_TMP_READY_INT. When the (MB number of written db temp+1) is greater than this filed in first MB line, trigger H264_DB_TMP_READY_INT. Min is 3. (R/W)

H264_B_REC_READY_TRIGGER_MB_LINES Configures when to trigger video sequence B H264_REC_READY_INT. When the MB line number of generated reconstruct pixel is greater than this filed, trigger H264_REC_READY_INT. Min is 4. (R/W)

H264_B_INTRA_COST_CMP_OFFSET Configures video sequence B intra cost offset when I MB compared with P MB. (R/W)


Register 39.24. H264_B_DECSCORE_REG (0x005C)

| 31 | 20   | 19             | 10     | 9       | 0         |
|-----|------|----------------|--------|---------|-----------|
| 0   | 0    |                |        |         |           |

H264_B_C_DECSCORE Configures video sequence B chroma MB decimate score. When chroma score is smaller than it, chroma decimate will be enabled. (R/W)

H264_B_L_DECSCORE Configures video sequence B luma MB decimate score. When luma score is smaller than it, luma decimate will be enabled. (R/W)
```