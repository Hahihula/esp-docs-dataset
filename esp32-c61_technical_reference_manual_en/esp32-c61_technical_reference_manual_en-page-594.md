

```markdown
Register 11.104. PAU_REGDMA_BKP_CONF_REG (0x002C)

| 31 | 22 | 21 | 17 | 16 | 7 | 6 | 0 |
|-----|-----|-----|----|----|---|---|---|
|     |     |     |    |    |   |   | Reset |
| 500 |     | 8   |    |    |   | 32|     |

PAU_READ_INTERVAL Configures the read interval for the link. (R/W)
PAU_LINK_TOUT_THRES Configures the link wait timeout threshold. (R/W)
PAU_BURST_LIMIT Configures the burst limit. (R/W)
PAU_BACKUP_TOUT_THRES Configures the backup timeout threshold. (R/W)

Register 11.105. PAU_INT_ENA_REG (0x0030)

| 31 | ... | 2 | 1 | 0 |
|-----|------|---|---|---|
|     |      |   |   | Reset |

PAU_DONE_INT_ENA Write 1 to enable backup done interrupt. (R/W)
PAU_ERROR_INT_ENA Write 1 to enable error interrupt. (R/W)

Register 11.106. PAU_INT_RAW_REG (0x0034)

| 31 | ... | 2 | 1 | 0 |
|-----|------|---|---|---|
|     |      |   |   | Reset |

PAU_DONE_INT_RAW The raw interrupt status for backup completion. (R/WTC/SS)
PAU_ERROR_INT_RAW The raw interrupt status for errors. (R/WTC/SS)
```