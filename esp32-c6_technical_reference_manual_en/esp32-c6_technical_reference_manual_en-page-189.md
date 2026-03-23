

```markdown
## 6.3.3 Reading of Parameters by Users

Users cannot read eFuse bits directly. The eFuse controller hardware reads all eFuse bits and stores the results to their corresponding registers in its memory space. Then, users can read eFuse bits by reading the registers that start with `EFUSE_RD_`. Details are provided in Table 6.3-4.

### Table 6.3-4. Registers Information

| BLOCK | Read Registers                                       | Registers When Programming This Block                     |
|-------|------------------------------------------------------|-----------------------------------------------------------|
| 0     | EFUSE_RD_WR_DIS_REG                                  | EFUSE_PGM_DATA0_REG                                      |
| 0     | EFUSE_RD_REPEAT_DATA0 ~ 4_REG                        | EFUSE_PGM_DATA1 ~ 5_REG                                  |
| 1     | EFUSE_RD_MAC_SPI_SYS0 ~ 5_REG                        | EFUSE_PGM_DATA0 ~ 5_REG                                  |
| 2     | EFUSE_RD_SYS_DATA_PART10 ~ 7_REG                     | EFUSE_PGM_DATA0 ~ 7_REG                                  |
| 3     | EFUSE_RD_USR_DATA0 ~ 7_REG                           | EFUSE_PGM_DATA0 ~ 7_REG                                  |
| 4-9   | EFUSE_RD_KEYn_DATA0 ~ 7_REG (n: 0 ~ 5)                | EFUSE_PGM_DATA0 ~ 7_REG                                  |
| 10    | EFUSE_RD_SYS_DATA_PART20 ~ 7_REG                     | EFUSE_PGM_DATA0 ~ 7_REG                                  |

### Updating reading data registers

The eFuse controller reads eFuse memory to update corresponding registers. This read operation happens at system reset and can also be triggered manually by users as needed (e.g., if new eFuse values have been programmed). The process of triggering a read operation by users is as follows:

1. Configure the field `EFUSE_OP_CODE` in register `EFUSE_CONF_REG` to 0x5AA5.
2. Configure the field `EFUSE_READ_CMD` in register `EFUSE_CMD_REG` to 1.
3. Poll register `EFUSE_CMD_REG` until it is 0x0, or wait for a `READ_DONE` interrupt. Information on how to identify a PGM_DONE or READ_DONE interrupt is provided below in this section.
4. Read the values of each parameter from eFuse memory.

The eFuse read registers will hold all values until the next read operation.

### Error detection

Error record registers allow users to detect if there is any inconsistency between the parameter read by eFuse controller and that in eFuse memory.

Registers `EFUSE_RD_REPEAT_ERR0 ~ 3_REG` indicate if there are any errors in programming parameters (except `EFUSE_WR_DIS`) to BLOCK0. The value 1 indicates an error is detected in programming the corresponding bit. The value 0 indicates no error.

Registers `EFUSE_RD_RS_ERR0 ~ 1_REG` store the number of corrected bytes as well as the result of RS decoding when eFuse controller reads BLOCK1 ~ BLOCK10.

The values of the above registers will be updated every time the reading data registers of eFuse controller have been updated.

### Identifying program/read operation

The methods to identify the completion of a program/read operation are described below. Please note that bit 1 corresponds to a program operation, and bit 0 corresponds to a read operation.
```