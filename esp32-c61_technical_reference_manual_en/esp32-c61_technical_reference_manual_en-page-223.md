

```markdown
| Name                                       | Description                                                                 | Address   | Access |
|--------------------------------------------|-----------------------------------------------------------------------------|-----------|--------|
| EFUSE_RD_KEY4_DATA6_REG                   | Register 6 of BLOCK8 (KEY4)                                                | 0x0134    | RO     |
| EFUSE_RD_KEY4_DATA7_REG                   | Register 7 of BLOCK8 (KEY4)                                                | 0x0138    | RO     |
| EFUSE_RD_KEY5_DATA0_REG                   | Register 0 of BLOCK9 (KEY5)                                                | 0x013C    | RO     |
| EFUSE_RD_KEY5_DATA1_REG                   | Register 1 of BLOCK9 (KEY5)                                                | 0x0140    | RO     |
| EFUSE_RD_KEY5_DATA2_REG                   | Register 2 of BLOCK9 (KEY5)                                                | 0x0144    | RO     |
| EFUSE_RD_KEY5_DATA3_REG                   | Register 3 of BLOCK9 (KEY5)                                                | 0x0148    | RO     |
| EFUSE_RD_KEY5_DATA4_REG                   | Register 4 of BLOCK9 (KEY5)                                                | 0x014C    | RO     |
| EFUSE_RD_KEY5_DATA5_REG                   | Register 5 of BLOCK9 (KEY5)                                                | 0x0150    | RO     |
| EFUSE_RD_KEY5_DATA6_REG                   | Register 6 of BLOCK9 (KEY5)                                                | 0x0154    | RO     |
| EFUSE_RD_KEY5_DATA7_REG                   | Register 7 of BLOCK9 (KEY5)                                                | 0x0158    | RO     |
| EFUSE_RD_SYS_PART2_DATA0_REG              | Register 0 of BLOCK10 (system)                                             | 0x015C    | RO     |
| EFUSE_RD_SYS_PART2_DATA1_REG              | Register 1 of BLOCK10 (system)                                             | 0x0160    | RO     |
| EFUSE_RD_SYS_PART2_DATA2_REG              | Register 2 of BLOCK10 (system)                                             | 0x0164    | RO     |
| EFUSE_RD_SYS_PART2_DATA3_REG              | Register 3 of BLOCK10 (system)                                             | 0x0168    | RO     |
| EFUSE_RD_SYS_PART2_DATA4_REG              | Register 4 of BLOCK10 (system)                                             | 0x016C    | RO     |
| EFUSE_RD_SYS_PART2_DATA5_REG              | Register 5 of BLOCK10 (system)                                             | 0x0170    | RO     |
| EFUSE_RD_SYS_PART2_DATA6_REG              | Register 6 of BLOCK10 (system)                                             | 0x0174    | RO     |
| EFUSE_RD_SYS_PART2_DATA7_REG              | Register 7 of BLOCK10 (system)                                             | 0x0178    | RO     |
| Report Register                           |                                                                             |           |        |
| EFUSE_RD_REPEAT_DATA_ERR0_REG             | Programming error record register 0 of BLOCK0                             | 0x017C    | RO     |
| EFUSE_RD_REPEAT_DATA_ERR1_REG             | Programming error record register 1 of BLOCK0                             | 0x0180    | RO     |
| EFUSE_RD_REPEAT_DATA_ERR2_REG             | Programming error record register 2 of BLOCK0                             | 0x0184    | RO     |
| EFUSE_RD_REPEAT_DATA_ERR3_REG             | Programming error record register 3 of BLOCK0                             | 0x0188    | RO     |
| EFUSE_RD_REPEAT_DATA_ERR4_REG             | Programming error record register 4 of BLOCK0                             | 0x018C    | RO     |
| RS block error report registers           |                                                                             |           |        |
| EFUSE_RD_RS_DATA_ERR0_REG                 | Programming error record register 0 of BLOCK1-10                          | 0x0190    | RO     |
| EFUSE_RD_RS_DATA_ERR1_REG                 | Programming error record register 1 of BLOCK1-10                          | 0x0194    | RO     |
| Version Control Register                  |                                                                             |           |        |
| EFUSE_DATE_REG                            | Version control register                                                   | 0x0198    | R/W    |
| Configuration Register                    |                                                                             |           |        |
| EFUSE_CLK_REG                             | eFuse clock configuration register                                        | 0x01C8    | R/W    |
| EFUSE_CONF_REG                            | eFuse operation mode configuration register                                | 0x01CC    | R/W    |
| EFUSE_DAC_CONF_REG                        | Controls the eFuse programming voltage                                    | 0x01E8    | R/W    |
| EFUSE_RD_TIM_CONF_REG                     | Configures read timing parameters                                          | 0x01EC    | R/W    |
| EFUSE_WR_TIM_CONF1_REG                    | Configures register 1 of eFuse programming timing parameters               | 0x01FO    | R/W    |
```