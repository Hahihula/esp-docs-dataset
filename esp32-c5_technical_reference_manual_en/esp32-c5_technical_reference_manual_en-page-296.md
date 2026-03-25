

```markdown
Register 7.38. EFUSE_WR_TIM_CONFO_RS_BYPASS_REG (0x01FC)
```

| Bit Range | Field Name                          | Description                                                                 |
|-----------|-------------------------------------|-----------------------------------------------------------------------------|
| 31        | (reserved)                         |                                                                             |
| 21-20     | EFUSE_BYPASS_RS_BLK_NUM            | Configures which block number to bypass the Reed-Solomon (RS) correction step. (R/W)<br>Options:<br>- 0: Update<br>- 1: No effect (WT) |
| 13        | EFUSE_UPDATE                       | Configures whether to update multi-bit register signals.<br>Options:<br>- 0: No effect (WT)<br>- 1: Update |
| 12-11     | EFUSE_TPGM_INACTIVE                | Configures the inactive programming time. Measurement unit: One cycle of the eFuse core clock. (R/W) |
| 1-0       | EFUSE_BYPASS_RS_CORRECTION         | Configures whether to bypass the Reed-Solomon (RS) correction step.<br>Options:<br>- 0: Not bypass<br>- 1: Bypass (R/W) |

```markdown
EFUSE_BYPASS_RS_CORRECTION Configures whether to bypass the Reed-Solomon (RS) correction step.
- 0: Not bypass
- 1: Bypass (R/W)

EFUSE_BYPASS_RS_BLK_NUM Configures which block number to bypass the Reed-Solomon (RS) correction step. (R/W)

EFUSE_UPDATE Configures whether to update multi-bit register signals.
- 1: Update
- 0: No effect (WT)

EFUSE_TPGM_INACTIVE Configures the inactive programming time. Measurement unit: One cycle of the eFuse core clock. (R/W)
```