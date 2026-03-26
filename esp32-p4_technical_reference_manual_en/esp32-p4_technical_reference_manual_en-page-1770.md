

# 37.9 Registers

The addresses in this section are relative to the Pixel-Processing Accelerator base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

## Register 37.1. PPA_BLEndo_CLUT_DATA_REG (0x0000)

```
PPA_RDWR_WORD_BLEndo_CLUT
31                                 0
+-----------------------------------------------+
|       0x000000        | Reset |
+-----------------------------------------------+
```

**PPA_RDWR_WORD_BLEndo_CLUT** Configures BLEND background layer CLUT access in FIFO mode. (R/W)

## Register 37.2. PPA_BLEND1_CLUT_DATA_REG (0x0004)

```
PPA_RDWR_WORD_BLEND1_CLUT
31                                 0
+-----------------------------------------------+
|       0x000000        | Reset |
+-----------------------------------------------+
```

**PPA_RDWR_WORD_BLEND1_CLUT** Configures BLEND foreground layer CLUT access in FIFO mode. (R/W)