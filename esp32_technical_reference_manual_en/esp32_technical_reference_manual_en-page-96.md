**Chapter 5 eFuse Controller (EFUSE)**

---

### System parameter table:

| Name                | Width | Bit       | Name                   |
|---------------------|-------|-----------|------------------------|
| SPI_pad_config_d   | 5     | [4:0]     |                        |
| SPI_pad_config_cs0 | 5     | [4:0]     |                        |
| vol_level_hp_inv   | 2     | [1:0]     |                        |
| dig_vol_16         | 4     | [3:0]     |                        |
| flash_crypt_config | 4     | [3:0]     |                        |
| coding_scheme       | 2     | [1:0]     |                        |
| console_debug_disable | 1   | [0]      | EFUSE_BLK0_WDATA6_REG |
| abstract_done_0    | -     | [0]       |                        |
| abstract_done_1    | -     | [0]       |                        |
| JTAG.disable        | -     | [0]       |                        |
| download_dis_encrypt | 1   | [0]      |                        |
| download_dis_decrypt | 1   | [0]      |                        |
| download_dis_cache | 1     | [0]       |                        |
| key_status         | 1     | [0]       |                        |

#### BLOCK1:
- 256/192/128
- EFUSE_BLK1_WDATA0_REG: [31:0]
- EFUSE_BLK1_WDATA1_REG: [31:0]
- EFUSE_BLK1_WDATA2_REG: [31:0]
- EFUSE_BLK1_WDATA3_REG: [31:0]
- EFUSE_BLK1_WDATA4_REG: [31:0]
- EFUSE_BLK1_WDATA5_REG: [31:0]
- EFUSE_BLK1_WDATA6_REG: [31:0]
- EFUSE_BLK1_WDATA7_REG: [31:0]

#### BLOCK2:
- 256/192/128
- EFUSE_BLK2_WDATA0_REG: [31:0]
- EFUSE_BLK2_WDATA1_REG: [31:0]
- EFUSE_BLK2_WDATA2_REG: [31:0]
- EFUSE_BLK2_WDATA3_REG: [31:0]
- EFUSE_BLK2_WDATA4_REG: [31:0]
- EFUSE_BLK2_WDATA5_REG: [31:0]
- EFUSE_BLK2_WDATA6_REG: [31:0]
- EFUSE_BLK2_WDATA7_REG: [31:0]

#### BLOCK3:
- 256/192/128
- EFUSE_BLK3_WDATA0_REG: [31:0]
- EFUSE_BLK3_WDATA1_REG: [31:0]
- EFUSE_BLK3_WDATA2_REG: [31:0]
- EFUSE_BLK3_WDATA3_REG: [31:0]
- EFUSE_BLK3_WDATA4_REG: [31:0]
- EFUSE_BLK3_WDATA5_REG: [31:0]
- EFUSE_BLK3_WDATA6_REG: [31:0]
- EFUSE_BLK3_WDATA7_REG: [31:0]

---

### Instructions:

The process of programming system parameters is as follows:
1. Configure EFUSE_CLK_SEL bit, EFUSE_CLK_SEL bit of register EFUSE_CLK, and EFUSE_DAC_CLK_DIV bit of register EFUSE_DAC_CONF.
2. Set the corresponding register bit of the system parameter bit to be programmed to 1.

---

**Footer:**
- Page number: 96
- Document version: ESP32 TRM (Version 5.6)
- Link for submitting documentation feedback

--- 

### Diagrams and Images:
There are no diagrams or flowcharts in this page, only a table of system parameters with their respective bit positions.

---

**Note:** The text has been transcribed as accurately as possible from the image provided without any additional interpretation beyond what is visible.