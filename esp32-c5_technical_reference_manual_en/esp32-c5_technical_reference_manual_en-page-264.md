

```markdown
| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| Programming Data Registers                 |                                                                                               |           |        |
| EFUSE_PGM_DATA0_REG                        | Register 0 that stores data to be programmed                                               | 0x0000    | R/W    |
| EFUSE_PGM_DATA1_REG                        | Register 1 that stores data to be programmed                                               | 0x0004    | R/W    |
| EFUSE_PGM_DATA2_REG                        | Register 2 that stores data to be programmed                                               | 0x0008    | R/W    |
| EFUSE_PGM_DATA3_REG                        | Register 3 that stores data to be programmed                                               | 0x000C    | R/W    |
| EFUSE_PGM_DATA4_REG                        | Register 4 that stores data to be programmed                                               | 0x0010    | R/W    |
| EFUSE_PGM_DATA5_REG                        | Register 5 that stores data to be programmed                                               | 0x0014    | R/W    |
| EFUSE_PGM_DATA6_REG                        | Register 6 that stores data to be programmed                                               | 0x0018    | R/W    |
| EFUSE_PGM_DATA7_REG                        | Register 7 that stores data to be programmed                                               | 0x001C    | R/W    |
| EFUSE_PGM_CHECK_VALUE0_REG                 | Register 0 that stores the RS code to be programmed                                        | 0x0020    | R/W    |
| EFUSE_PGM_CHECK_VALUE1_REG                 | Register 1 that stores the RS code to be programmed                                        | 0x0024    | R/W    |
| EFUSE_PGM_CHECK_VALUE2_REG                 | Register 2 that stores the RS code to be programmed                                        | 0x0028    | R/W    |

Reading Data Registers for BLOCK0
| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| EFUSE_RD_WR_DIS_REG                        | BLOCK0 data register 0 that represents whether programming of individual eFuse memory bit is disabled | 0x002C    | RO     |
| EFUSE_RD_REPEAT_DATA0_REG                  | BLOCK0 data register 1                                                                         | 0x0030    | RO     |
| EFUSE_RD_REPEAT_DATA1_REG                  | BLOCK0 data register 2                                                                         | 0x0034    | RO     |
| EFUSE_RD_REPEAT_DATA2_REG                  | BLOCK0 data register 3                                                                         | 0x0038    | RO     |
| EFUSE_RD_REPEAT_DATA3_REG                  | BLOCK0 data register 4                                                                         | 0x003C    | RO     |
| EFUSE_RD_REPEAT_DATA4_REG                  | BLOCK0 data register 5                                                                         | 0x0040    | RO     |

Reading Data Registers for BLOCK1
| Name                                       | Description                                                                                   | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------------------------|-----------|--------|
| EFUSE_RD_MAC_SYSO_REG                      | Register 0 for BLOCK1                                                                          | 0x0044    | RO     |
| EFUSE_RD_MAC_SYS1_REG                      | Register 1 for BLOCK1                                                                          | 0x0048    | RO     |
| EFUSE_RD_MAC_SYS2_REG                      | Register 2 for BLOCK1                                                                          | 0x004C    | RO     |
| EFUSE_RD_MAC_SYS3_REG                      | Register 3 for BLOCK1                                                                          | 0x0050    | RO     |
```