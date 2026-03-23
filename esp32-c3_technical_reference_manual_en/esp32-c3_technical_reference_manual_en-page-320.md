

```markdown
| Internal Memory A | Instruction / Data Regions | Split Regions B |
|:-------------------|:----------------------------|:-----------------|
|                   | Instruction Region         | Instr_Region_0  |
| SRAM1              |                            | Instr_Region_1  |
|                   | Data Region                | Instr_Region_2  |
|                   |                            | Data_Region_0   |
|                   |                            | Data_Region_1   |
|                   |                            | Data_Region_2   |

A Access to each split region can be configured independently. See details in Table 14.4-6 and 14.4-7.
B See the description below on how to configure the split lines.

Internal SRAM1 Split Regions

ESP32-C3 allows users to configure the split lines to their needs with registers below:

*   Split line to split the Instruction and Data regions (IRamO_DRamO_split_line):
    - PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE_CONSTRAIN_1_REG
*   The first split line to further split the Instruction Region (IRamO_split_line_0):
    - PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE_CONSTRAIN_2_REG
*   The second split line to further split the Instruction Region (IRamO_split_line_1):
    - PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE_CONSTRAIN_3_REG
*   The first split line to further split the data Region (DRamO_split_line_0):
    - PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE_CONSTRAIN_4_REG
*   The second split line to further split the data Region (DRamO_split_line_1):
    - PMS_CORE_X_IRAMO_DRAMO_DMA_SPLIT_LINE_CONSTRAIN_5_REG

When configuring the split lines,

1.  First configure the block in which the split line is by:
    *   Configuring the Category_X field for the block in which the split line is to 0x1 or 0x2 (no difference)
    *   Configuring the Category_0 ~ Category_X-1 fields for all the preceding blocks to 0x0
    *   Configuring the Category_X+1 ~ Category_2 fields for all blocks afterwards to 0x3

For example, assuming you want to configure the split line in Block1, then first configure the Category_1 field for Block1 to 0x1 or 0x2; configure the Category_0 for Block0 to 0x0; and configure the Category_2 for Block2 to 0x3 (see illustration in Figure 14.4-2). On the other hand, when reading 0x1 or 0x2 from Category_1, then you know the split line is in Block1.

2.  Configure the position of the split line inside the configured block by:
    *   Writing the [16:9] bits of the actual address at which you want to split the memory to the SPLITADDR field for the block in which the split line is.
    *   Note that the split address must be aligned to 512 bytes, meaning you can only write the integral multiples of 0x200 to the SPLITADDR field.
```