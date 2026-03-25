

# Chapter 5 eFuse Controller (EFUSE)

## 5.7 Registers

The addresses in this section are relative to eFuse controller base address provided in Table 4.3-2 in Chapter 4 System and Memory.

### Register 5.1. EFUSE_PGM_DATAₙ_REG (n: 0-7) (0x0000+0x4*n)

EFUSE_PGM_DATAₙ Configures the nth 32-bit data to be programmed. (R/W)

```
31                                 0
+-------------------------------------+
|         0x000000          | Reset
+-------------------------------------+
```

### Register 5.2. EFUSE_PGM_CHECK_VALUEₙ_REG (n: 0-2) (0x0020+0x4*n)

EFUSE_PGM_RS_DATAₙ Configures the nth RS code to be programmed. (R/W)

```
31                                 0
+-------------------------------------+
|         0x000000          | Reset
+-------------------------------------+
```

### Register 5.3. EFUSE_RD_WR_DISO_REG (0x002C)

EFUSE_WR_DIS Represents whether programming of individual eFuse memory bit is disabled or enabled.
1: Disabled
0: Enabled
(RO)