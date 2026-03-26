

```markdown
Register 37.22. PPA_INT_RAW_REG (0x0010)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 4   | Reset                                                                      |
| 3   | PPA_BLEND_PARAM_CFG_ERR_INT_RAW                                            |
| 2   | PPA_SRM_PARAM_CFG_ERR_INT_RAW                                              |
| 1   | PPA_BLEND_EOF_INT_RAW                                                       |
| 0   | PPA_SRM_EOF_INT_RAW                                                         |

PPA_SRM_EOF_INT_RAW The raw interrupt status of PPA_SRM_EOF_INT.
(R/WTC/SS)

PPA_BLEND_EOF_INT_RAW The raw interrupt status of PPA_BLEND_EOF_INT.
(R/WTC/SS)

PPA_SRM_PARAM_CFG_ERR_INT_RAW The raw interrupt status of
PPA_SRM_PARAM_CFG_ERR_INT. Check PPA_SRM_PARAM_ERR_ST_REG to get the specific error.
(R/WTC/SS)

PPA_BLEND_PARAM_CFG_ERR_INT_RAW The raw interrupt status of
PPA_BLEND_PARAM_CFG_ERR_INT. Check PPA_BLEND_ST_REG to get the specific error.
(R/WTC/SS)
```