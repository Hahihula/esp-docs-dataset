

```markdown
Register 39.4. H264_A_SYS_CONF_REG (0x000C)

| 31 | 30     | 29             | 14 | 13       | 7   | 6              | Reset |
|-----|--------|----------------|----|----------|-----|----------------|-------|
| 0   | 0      |                |    |          | 4   | 3              |       |

H264_A_DB_TMP_READY_TRIGGER_MB_NUM Configures when to trigger video sequence A H264_DB_TMP_READY_INT. When the (MB number of written db temp+1) is greater than this filed in first MB line, trigger H264_DB_TMP_READY_INT. Min is 3. (R/W)

H264_A_REC_READY_TRIGGER_MB_LINES Configures when to trigger video sequence A H264_REC_READY_INT. When the MB line number of generated reconstruct pixel is greater than this filed, trigger H264_REC_READY_INT. Min is 4. (R/W)

H264_A_INTRACOST_CMP_OFFSET Configures video sequence A intra cost offset when I MB compared with P MB. (R/W)
```

```markdown
Register 39.5. H264_A_DECSCORE_REG (0x0010)

| 31 | 20   | 19             | 10 | 9        | Reset |
|-----|------|----------------|----|----------|-------|
| 0   | 0    |                |    |          |       |

H264_A_C_DECSCORE Configures video sequence A chroma MB decimate score. When chroma score is smaller than it, chroma decimate will be enabled. (R/W)

H264_A_L_DECSCORE Configures video sequence A luma MB decimate score. When luma score is smaller than it, luma decimate will be enabled. (R/W)
```