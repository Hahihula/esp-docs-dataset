

```markdown
Register 20.100. LP_SYSTEM_HP_POR_RST_BYPASS_CTRL_REG (0x01A0)

| Bit | 31 | 24 | 23 | 16 | 15 | 8 | 7 | 0 |
|-----|----|----|----|----|----|---|---|---|
|     | Oxff | 0 | 0 | 0 | 0 | 0 | 0 | Reset |

LP_SYSTEM_HP_PO_CNNT_RSTN_BYPASS_CTRL Configures whether or not to bypass a certain reset source for the HP_CNNT power domain during the Power-On reset.
- 0: No effect
- 1: Bypass
See section 20.2.2.5 for detailed information about respective fields. (R/W)

LP_SYSTEM_HP_PO_RSTN_BYPASS_CTRL configures whether or not to bypass the following reset sources for the HP power domain during the Power-On reset.
- 0: No effect
- 1: Bypass
See section 20.2.2.5 for detailed information about respective fields. (R/W)
```