

# Chapter 6 eFuse Controller

## 6.5 Registers

The addresses in this section are relative to eFuse controller base address provided in Table 5.3-2 in Chapter 5 System and Memory.

### Register 6.1. EFUSE_PGM_DATA0_REG (0x0000)

EFUSE_PGM_DATA_0 Configures the 0th 32-bit data to be programmed. (R/W)

```
31                                 0
+-------------------------------------+
|             0x000000              |
+-------------------------------------+
Reset
```

### Register 6.2. EFUSE_PGM_DATA1_REG (0x0004)

EFUSE_PGM_DATA_1 Configures the 1st 32-bit data to be programmed. (R/W)

```
31                                 0
+-------------------------------------+
|             0x000000              |
+-------------------------------------+
Reset
```

### Register 6.3. EFUSE_PGM_DATA2_REG (0x0008)

EFUSE_PGM_DATA_2 Configures the 2nd 32-bit data to be programmed. (R/W)

```
31                                 0
+-------------------------------------+
|             0x000000              |
+-------------------------------------+
Reset
```