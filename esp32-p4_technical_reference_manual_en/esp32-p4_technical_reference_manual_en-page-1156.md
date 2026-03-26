

# 19.7 Registers

## 19.7.1 HP_DMA_PMS_REG

The addresses in this section are relative to the HP_DMA_PMS base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 19.1. PMS_DMA_DATE_REG (0x0000)

```
PMS_DMA_DATE
31                                 0
+-----------------------------------------------+
|                0x20230314                 |
+-----------------------------------------------+
Reset

PMS_DMA_DATE Version control register. (R/W)
```

### Register 19.2. PMS_DMA_CLK_EN_REG (0x0004)

```
(reserved)
31                                 0
+-----------------------------------------------+
|                0x00000001                 |
+-----------------------------------------------+
Reset

PMS_DMA_CLK_EN Configures whether to keep the clock always on.
0: Enable automatic clock gating.
1: Keep the clock always on.
(R/W)
```

### Register 19.3. PMS_DMA_REGIONn_LOW_REG (n: 0-31) (0x0008+0x8*n)

```
PMS_DMA_REGIONn_LOW
31                                 12   11           0
+-----------------------------------------------+
|                0x0000                 |
+-----------------------------------------------+
(reserved)
Reset

PMS_DMA_REGIONn_LOW Configures the high 20 bits of the start address for regionn. (R/W)
```