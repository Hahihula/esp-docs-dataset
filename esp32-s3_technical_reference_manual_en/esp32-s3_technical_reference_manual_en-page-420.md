**Chapter Title:**
Chapter 5 eFuse Controller

**Section and Subsection Titles with Page Number:**
GoBack  
8.

**Body Text:**

Check error record registers. If the values read in error record registers are not O, the programming process should be performed again following above steps I ~7. Please check the following error record registers for different eFuse blocks:

- **BLOCK0:** EFUSE_RD_REPEAT_ERR0_REG ≈ EFUSE_RDRepeatErr4Reg
- **BLOCK1:** EFUSE_RDsysErr0Reg[2:0], EFUSE_RDsysErrReg[7]
- **BLOCK2:** EFUSE_RDsysErrReg[6:4], EFUSE_RDsysErrReg[11]
- **BLOCK3:** EFUSE_RDsysErrReg[10:8], EFUSE_RDsysErrReg[15]
- **BLOCK4:** EFUSE_RDsysErrReg[14:12], EFUSE_RDsysErrReg[19]
- **BLOCK5:** EFUSE_RDsysErrReg[18:16], EFUSE_RDsysErrReg[23]
- **BLOCK6:** EFUSE_RDsysErrReg[22:20], EFUSE_RDsysErrReg[27]
- **BLOCK7:** EFUSE_RDsysErrReg[26:24], EFUSE_RDsysErrReg[31]
- **BLOCK8:** EFUSE_RDsysErrReg[30:28], EFUSE_RDsysErrReg[3]
- **BLOCK9:** EFUSE_RDsysErrReg[2:0], EFUSE_RDsysErrReg[7]
- **BLOCK10:** EFUSE_RDsysErrReg[2:0][6:4]

**Subsection Title and Body Text with Limitations:**

Limitations

In BLOCKO, each bit can be programmed separately. However, we recommend to minimize programming cycles and program all the bits of a parameter in one programming action. In addition, after all parameters controlled by a certain bit of EFUSE_WRDis are programmed, that bit should immediately be programmed.

The programming of parameters controlled by a certain bit of EFUSE_WRDis, and the programming of the bit itself can even be completed at the same time. Repeated programming of already programmed bits is strictly forbidden, otherwise, programming errors will occur.
BLOCK1 cannot be programmed by users as it has been programmed at manufacturing.
BLOCK2 ~ 10 can only be programmed once. Repeated programming is not allowed.

**Subsection Title and Body Text with User Read of Parameters:**

5.3.3 User Read of Parameters

Users cannot read eFuse bits directly. The eFuse Controller hardware reads all eFuse bits and stores the results to their corresponding registers in its memory space. Then, users can read eFuse bits by reading the registers that start with EFUSE_RD_. Details are provided in Table 5.3-4.

**Table Title:**
Table 5.3-4. Registers Information

| BLOCK | Read Registers | Registers When Programming This Block |
|-------|-----------------|----------------------------------------|
|       |                 | EFUSE_PGM_DATA0_REG                    |
| 0     | EFUSE_RD_WR_DIS Reg | EFUSE_PGM_DATA1 ~ 5_REG                |
| 0     | EFUSE_RDRepeatDATAO ~ 4_REG           | EFUSE_PGM_DATA2 ~ 7_REG                |
| 1     | EFUSE_RD_MAC_SPI_SYS_0 ~ 5_REG       | EFUSE_PGM_DATA3 ~ 6_REG                |
| 2     | EFUSE_RDsysPart1_0 ~ 7_REG           | EFUSE_PGM_DATA4 ~ 8_REG                |
| 3     | EFUSE_RDsysDATAO ~ 7_REG             | EFUSE_PGM_DATA5 ~ 9_REG                |
| 4 ~ 9 | EFUSE_RD_KEYn_DATAO (n:0~5)         | EFUSE_PGM_DATA6 ~ 12_REG               |
| 10    | EFUSE_RDsysPart2_0 ~ 7_REG           | EFUSE_PGM_DATA13 ~ 18_REG              |

**Footer Text with Company and Document Information:**
Espressif Systems  
420 ESP32-S3 TRM (Version 1.7)