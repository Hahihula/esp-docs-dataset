

```markdown
| BLOCK | Read Registers                                                                 |
|-------|---------------------------------------------------------------------------------|
| 3     | EFUSE_RD_USR_DATAn_REG (n: 0 ~ 7)                                               |
| 4-9   | EFUSE_RD_KEYn_DATAm_REG (n: 0 ~ 5) (m: 0 ~ 7)                                   |
| 10    | EFUSE_RD_SYS_PART2_DATAn_REG (n: 0 ~ 7)                                         |

Table 7.3-4 – cont’d from previous page

<table><thead><tr><th>BLOCK</th><th>Read Registers</th><th>Registers When Programming This Block</th></tr></thead><tbody><tr><td>3</td><td>EFUSE_RD_USR_DATAn_REG (n: 0 ~ 7)</td><td>EFUSE_PGM_DATAn_REG (n: 0 ~ 7)</td></tr><tr><td>4-9</td><td>EFUSE_RD_KEYn_DATAm_REG (n: 0 ~ 5) (m: 0 ~ 7)</td><td>EFUSE_PGM_DATAn_REG (n: 0 ~ 7)</td></tr><tr><td>10</td><td>EFUSE_RD_SYS_PART2_DATAn_REG (n: 0 ~ 7)</td><td>EFUSE_PGM_DATAn_REG (n: 0 ~ 7)</td></tr></tbody></table>

Updating reading data registers

The eFuse controller reads eFuse memory to update corresponding registers. This read operation happens at system reset and can also be triggered manually by users as needed (e.g., if new eFuse values have been programmed). The process of triggering a read operation by users is as follows:

1. Configure the field EFUSE_OP_CODE in register EFUSE_CONF_REG to 0x5AA5.
2. Configure the field EFUSE_READ_CMD in register EFUSE_CMD_REG to 1.
3. Poll register EFUSE_CMD_REG until it is 0x0, or wait for a READ_DONE interrupt. Information on how to identify a PGM_DONE or READ_DONE interrupt is provided below in this section.
4. Read the values of each parameter from eFuse memory.

The eFuse read registers will hold all values until the next read operation.

Error detection

The programming error record registers allow users to check the integrity of parameters stored in the eFuse memory. For instance, they can help detect whether the four-backup parameters are consistent and whether parameters protected by RS encoding are decoded successfully.

Registers EFUSE_RD_REPEAT_DATA_ERRn_REG (n: 0 ~ 3) indicate if there are any errors in programming parameters (except EFUSE_WR_DIS) to BLOCK0. The value 1 indicates an error is detected in programming the corresponding bit. The value 0 indicates no error.

Registers EFUSE_RD_RS_DATA_ERRn_REG (n: 0 ~ 1) store the number of corrected bytes as well as the result of RS decoding when eFuse controller reads BLOCK1 ~ BLOCK10.

The values of the above registers will be updated every time the reading data registers of eFuse controller have been updated.

Identifying completion of program or read operations

The methods to identify the completion of a program/read operation are described below. Please note that bit 1 corresponds to a program operation, and bit 0 corresponds to a read operation.

* Method one: Poll bit 1/0 in register EFUSE_INT_RAW_REG until it becomes 1, which represents the completion of a program/read operation.
* Method two:

    1. Set bit 1/0 in register EFUSE_INT_ENA_REG to 1 to enable the eFuse controller to post a PGM_DONE or READ_DONE interrupt.
    2. Configure the Interrupt Matrix to enable the CPU to respond to eFuse interrupt signals. See Chapter 11 Interrupt Matrix.
    3. Wait for the PGM_DONE or READ_DONE interrupt.
```