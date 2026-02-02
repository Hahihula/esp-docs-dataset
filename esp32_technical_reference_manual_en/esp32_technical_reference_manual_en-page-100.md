**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Table of System Parameters**

| Name       | Bit Width | Bit Range   | Name                          | Register                   | Bit |
|------------|-----------|-------------|-------------------------------|-----------------------------|-----|
| BLOCK1     |           |             |                               |                            |     |
|            | 256/192/128 | [31:0]       | EFUSE_BLK1_RDATA0_REG        |                           | [31:0] |
|            |           | [63:32]      | EFUSE_BLK1_RDATA1_REG        |                           | [31:0] |
|            |           | [95:64]      | EFUSE_BLK1_RDATA2_REG        |                           | [31:0] |
|            |           | [127:96]     | EFUSE_BLK1_RDATA3_REG        |                           | [31:0] |
|            |           | [159:128]    | EFUSE_BLK1_RDATA4_REG        |                           | [31:0] |
|            |           | [191:160]    | EFUSE_BLK1_RDATA5_REG        |                           | [31:0] |
|            |           | [223:192]    | EFUSE_BLK1_RDATA6_REG        |                           | [31:0] |
| BLOCK2     | 256/192/128 | [31:0]       | EFUSE_BLK2_RDATA0_REG        |                           | [31:0] |
|            |           | [63:32]      | EFUSE_BLK2_RDATA1_REG        |                           | [31:0] |
|            |           | [95:64]      | EFUSE_BLK2_RDATA2_REG        |                           | [31:0] |
|            |           | [127:96]     | EFUSE_BLK2_RDATA3_REG        |                           | [31:0] |
|            |           | [159:128]    | EFUSE_BLK2_RDATA4_REG        |                           | [31:0] |
|            |           | [191:160]    | EFUSE_BLK2_RDATA5_REG        |                           | [31:0] |
|            |           | [223:192]    | EFUSE_BLK2_RDATA6_REG        |                           | [31:0] |
| BLOCK3     | 256/192/128 | [31:0]       | EFUSE_BLK3_RDATA0_REG        |                           | [31:0] |
|            |           | [63:32]      | EFUSE_BLK3_RDATA1_REG        |                           | [31:0] |
|            |           | [95:64]      | EFUSE_BLK3_RDATA2_REG        |                           | [31:0] |
|            |           | [127:96]     | EFUSE_BLK3_RDATA3_REG        |                           | [31:0] |
|            |           | [159:128]    | EFUSE_BLK3_RDATA4_REG        |                           | [31:0] |
|            |           | [191:160]    | EFUSE_BLK3_RDATA5_REG        |                           | [31:0] |
|            |           | [223:192]    | EFUSE_BLK3_RDATA6_REG        |                           | [31:0] |
|            |           | [255:224]    | EFUSE_BLK3_RDATA7_REG        |                           | [31:0] |

**Section 5.3.4 The Use of System Parameters by Hardware Modules**

Hardware modules are directly hardwired to the ESP32 in order to use the system parameters. Software cannot change this behaviour. Hardware modules use the decoded values of system parameters BLOCK1, BLOCK2, and BLOCK3, not their encoded values.

**Section 5.3.5 Interrupts**

- EFUSE_PGM_DONE_INT: Triggered when eFuse programming has finished.
- EFUSE_READ_DONE_INT: Triggered when eFuse reading has finished.

**Section 5.4 Register Summary**

The addresses in this section are relative to the eFuse Controller base address provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory.

**Footer Information**
- Espressif Systems
- Page number: 100
- Document version: ESP32 TRM (Version 5.6)
- Submit Documentation Feedback