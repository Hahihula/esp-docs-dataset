

```markdown
| BLOCK | Read Registers                     | Registers When Programming This Block                  |
|-------|-------------------------------------|--------------------------------------------------------|
| 0     | EFUSE_RD_WR_DIS_REG                | EFUSE_PGM_DATABO_REG                                  |
| 0     | EFUSE_RD_REPEAT_DATA0 ~ 4_REG      | EFUSE_PGM_DATA1 ~ 5_REG                               |
| 1     | EFUSE_RD_MAC_SYS0 ~ 5_REG          | EFUSE_PGM_DATA0 ~ 5_REG                               |
| 2     | EFUSE_RD_SYS_PART1_DATA0 ~ 7_REG   | EFUSE_PGM_DATA0 ~ 7_REG                               |
| 3     | EFUSE_RD_USR_DATA0 ~ 7_REG         | EFUSE_PGM_DATA0 ~ 7_REG                               |
| 4-9   | EFUSE_RD_KEYn_DATA0 ~ 7_REG (n: 0 ~ 5) | EFUSE_PGM_DATA0 ~ 7_REG                              |
| 10    | EFUSE_RD_SYS_PART2_DATA0 ~ 7_REG   | EFUSE_PGM_DATA0 ~ 7_REG                               |

## Updating reading data registers

The eFuse controller reads eFuse memory to update corresponding registers. This read operation happens at system reset and can also be triggered manually by users as needed (e.g., if new eFuse values have been programmed). The process of triggering a read operation by users is as follows:

1. Configure the field `EFUSE_OP_CODE` in register `EFUSE_CONF_REG` to 0x5AA5.
2. Configure the field `EFUSE_READ_CMD` in register `EFUSE_CMD_REG` to 1.
3. Poll register `EFUSE_CMD_REG` until it is 0x0, or wait for a `READ_DONE` interrupt. Information on how to identify a `PGM_DONE` or `READ_DONE` interrupt is provided below in this section.
4. Read the values of each parameter from eFuse memory.

The eFuse read registers will hold all values until the next read operation.

## Error detection

The programming error record registers allows users to check the integrity of parameters stored in the eFuse memory. For instance, they can help detect whether the four-backup parameters are consistent and whether parameters protected by RS encoding are decoded successfully.

Registers `EFUSE_RD_REPEAT_ERRRO ~ 3_REG` indicate if there are any errors in programming parameters (except `EFUSE_WR_DIS`) to BLOCK0. The value 1 indicates an error is detected in programming the corresponding bit. The value 0 indicates no error.

Registers `EFUSE_RD_RS_ERRRO ~ 1_REG` store the number of corrected bytes as well as the result of RS decoding when eFuse controller reads BLOCK1 ~ BLOCK10.

The values of the above registers will be updated every time the reading data registers of eFuse controller have been updated.

## Identifying completion of program or read operations

The methods to identify the completion of a program/read operation are described below. Please note that bit 1 corresponds to a program operation, and bit 0 corresponds to a read operation.

* Method one: Poll bit 1/0 in register `EFUSE_INT_RAW_REG` until it becomes 1, which represents the completion of a program/read operation.
* Method two:

    1. Set bit 1/0 in register `EFUSE_INT_ENA_REG` to 1 to enable the eFuse controller to post a PGM_DONE or READ_DONE interrupt.
```