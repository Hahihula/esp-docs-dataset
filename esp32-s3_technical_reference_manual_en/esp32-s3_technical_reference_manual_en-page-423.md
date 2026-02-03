Title: Chapter 5 eFuse Controller

Subtitle: GoBack

Section Title:
5.4 Register Summary

Body Text:

The addresses in this section are relative to eFuse Controller base address provided in Table 4.3-3 in Chapter 4 System and Memory.

The abbreviations given in Column Access are explained in Section [Access Types for Registers](#).

Table Headers: 
- Name
- Description
- Address
- Access

Table Content:

**PGM Data Register**
- EFUSE_PGM_DATA0_REG | Register O that stores data to be programmed | 0x0000 | R/W
- EFUSE_PGM_DATA1_REG | Register 1 that stores data to be programmed | 0x0004 | R/W
- EFUSE_PGM_DATA2_REG | Register 2 that stores data to be programmed | 0x0008 | R/W
- EFUSE_PGM_DATA3_REG | Register 3 that stores data to be programmed | 0x000C | R/W
- EFUSE_PGM_DATA4_REG | Register 4 that stores data to be programmed | 0x0010 | R/W
- EFUSE_PGM_DATA5_REG | Register 5 that stores data to be programmed | 0x0014 | R/W
- EFUSE_PGM_DATA6_REG | Register 6 that stores data to be programmed | 0x0018 | R/W
- EFUSE_PGM_DATA7_REG | Register 7 that stores data to be programmed | 0x001C | R/W
- EFUSE_PGM_CHECK_VALUE0_REG | Register O that stores the RS code to be programmed | 0x0020 | R/W
- EFUSE_PGM_CHECK_VALUE1_REG | Register 1 that stores the RS code to be programmed | 0x0024 | R/W
- EFUSE_PGM_CHECK_VALUE2_REG | Register 2 that stores the RS code to be programmed | 0x0028 | R/W

**Read Data Register**
- EFUSE_RD_WR_DIS_REG | BLOCKO data register O | 0x002C | RO
- EFUSE_RD_REPEAT_DATA0_REG | BLOCKO data register 1 | 0x0030 | RO
- EFUSE_RDPEAT_DATA1_REG | BLOCKO data register 2 | 0x0034 | RO
- EFUSE_RDPEAT_DATA2_REG | BLOCKO data register 3 | 0x0038 | RO
- EFUSE_RDPEAT_DATA3_REG | BLOCKO data register 4 | 0x003C | RO
- EFUSE_RDPEAT_DATA4_REG | BLOCKO data register 5 | 0x0040 | RO
- EFUSE_RD_MAC_SPI_SYS_0_REG | BLOCK1 data register O | 0x0044 | RO
- EFUSE_RD_MAC_SPI_SYS_1_REG | BLOCK1 data register 1 | 0x0048 | RO
- EFUSE_RD_MAC_SPI_SYS_2_REG | BLOCK1 data register 2 | 0x004C | RO
- EFUSE_RD_MAC_SPI_SYS_3_REG | BLOCK1 data register 3 | 0x0050 | RO
- EFUSE_RD_MAC_SPI_SYS_4_REG | BLOCK1 data register 4 | 0x0054 | RO
- EFUSE_RD_MAC_SPI_SYS_5_REG | BLOCK1 data register 5 | 0x0058 | RO
- EFUSEsys_PART1_DATAO_REG | Register O of BLOCK2 (system) | 0x005C | RO
- EFUSEsys_PART1_DATA1_REG | Register 1 of BLOCK2 (system) | 0x0060 | RO
- EFUSEsys_PART1_DATA2_REG | Register 2 of BLOCK2 (system) | 0x0064 | RO
- EFUSEsys_PART1_DATA3_REG | Register 3 of BLOCK2 (system) | 0x0068 | RO
- EFUSEsys_PART1_DATA4_REG | Register 4 of BLOCK2 (system) | 0x006C | RO
- EFUSEsys_PART1_DATA5_REG | Register 5 of BLOCK2 (system) | 0x0070 | RO
- EFUSEsys_PART1_DATA6_REG | Register 6 of BLOCK2 (system) | 0x0074 | RO
- EFUSEsys_PART1_DATA7_REG | Register 7 of BLOCK2 (system) | 0x0078 | RO

Footer:
Espressif Systems  
Page Number: 423  
Document Version Information: ESP32-S3 TRM (Version 1.7)

Link Texts:

- [Access Types for Registers](#)

Navigation Link at the top right corner of each page.

(Note: The text "Submit Documentation Feedback" is present but not part of a section or table, so it's treated as an additional footer note.)