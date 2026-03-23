

```markdown
Register 4.11. EFUSE_PGM_CHECK_VALUE2_REG (0x0028)

EFUSE_PGM_RS_DATA_2

31                                 0
+-----------------------------------------------+
|       0x000000        Reset                  |
+-----------------------------------------------+

EFUSE_PGM_RS_DATA_2   The content of the 2nd 32-bit RS code to be programmed. (R/W)

Register 4.12. EFUSE_RD_WR_DIS_REG (0x002C)

EFUSE_WR_DIS

31                                 0
+-----------------------------------------------+
|       0x000000        Reset                  |
+-----------------------------------------------+

EFUSE_WR_DIS   Represents whether programming of corresponding eFuse part is disabled or enabled. 1: Disabled. 0: Enabled. (RO)
```