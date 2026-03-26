

```markdown
Register 37.25. PPA_INT_CLR_REG (0x001C)

| 31 | 4 | 3 | 2 | 1 | 0 |
|----:|:-|:-|:-|:-|:-|
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |

PPA_SRM_EOF_INT_CLR   Write 1 to clear PPA_SRM_EOF_INT. (WT)
PPA_BLEND_EOF_INT_CLR  Write 1 to clear PPA_BLEND_EOF_INT. (WT)
PPA_SRM_PARAM_CFG_ERR_INT_CLR Write 1 to clear PPA_SRM_PARAM_CFG_ERR_INT. (WT)
PPA_BLEND_PARAM_CFG_ERR_INT_CLR □ 1 □□ PPA_BLEND_PARAM_CFG_ERR_INT□ (WT)

Register 37.26. PPA_CLUT_CNT_REG (0x0070)

| 31 | 18   | 17 | 9 | 8 | 0 |
|----:|------|----:|:-|:-|:-|
| 0 0 0 0 0 0 0 0 0 0 0 0 O | OxO | OxO | Reset |

PPA_BLENDO_CLUT_CNT   Represents the current write address of the BLEND background layer CLUT in FIFO mode. (RO)
PPA_BLEND1_CLUT_CNT    Represents the current write address of the BLEND foreground layer CLUT in FIFO mode. (RO)
```