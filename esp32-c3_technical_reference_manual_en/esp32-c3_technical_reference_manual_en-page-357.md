

```markdown
| Bit Range | Field Name                                                                                      | Description                                                                                                                                                  |
|-----------|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31-22     | (reserved)                                                                                    | No operation.                                                                                                                                               |
| 21        | PMS_CORE_X_IRAMO_DRAMO_DMA_SRAM_CATEGORY_0                                                  | Configures Block0's category field for the instruction and data split line IRAMO_DRAMO_Split_Line. (R/WL)                                                     |
| 20        | PMS_CORE_X_IRAMO_DRAMO_DMA_SRAM_CATEGORY_1                                                  | Configures Block1's category field for the instruction and data split line IRAMO_DRAMO_Split_Line. (R/WL)                                                    |
| 19        | PMS_CORE_X_IRAMO_DRAMO_DMA_SRAM_CATEGORY_2                                                  | Configures Block2's category field for the instruction and data split line IRAMO_DRAMO_Split_Line. (R/WL)                                                   |
| 18-0      | PMS_CORE_X_IRAMO_DRAMO_DMA_SRAM_SPLITADDR                                                    | Configures the split address of the instruction and data split line IRAMO_DRAMO_Split_Line. (R/WL)                                                           |

Register 14.23. PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE_CONSTRAIN_1_REG (0x0094)
```