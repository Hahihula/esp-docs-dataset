

```markdown
| Bit     | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|---------|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| Value   | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |    | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_SPLITADDR | PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_CATEGORY_2 | PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_CATEGORY_1 | PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_CATEGORY_0 |
```


Register 14.27. PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE_CONSTRAIN_5_REG (0x00A4)

PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_CATEGORY_0 Configures Block0’s category field for data internal split line DRAMO_Split_Line_1. (R/WL)
PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_CATEGORY_1 Configures Block1’s category field for data internal split line DRAMO_Split_Line_1. (R/WL)
PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_CATEGORY_2 Configures Block2’s category field for data internal split line DRAMO_Split_Line_1. (R/WL)
PMS_CORE_X_DRAMO_DMA_SRAM_LINE_1_SPLITADDR Configures the split address of data internal split line DRAMO_Split_Line_1. (R/WL)
```