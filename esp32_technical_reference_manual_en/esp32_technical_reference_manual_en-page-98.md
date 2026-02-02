Title: Chapter 5 eFuse Controller (EFUSE)

Subtitle: 5.3.3 Software Reading of System Parameters

Body Text:
Each bit of the 30 fixed-length system parameters and the three variable-length system parameters corresponds to a software-read register bit, as shown in Table 5.3-5. Software can use the value of each system parameter by reading the value in the corresponding register.

The bit width of system parameters BLOCK1, BLOCK2, and BLOCK3 is variable. Although 256 register bits have been assigned to each of the three parameters, as shown in Table 5.3-5, some of the 256 register bits are useless in the 3/4 coding and the Repeat coding scheme. In the None coding scheme, the corresponding register bit of each bit of BLOCK1[255:0] is used. In the 3/4 coding scheme, only the corresponding register bits of BLOCKN[191:0] are useful. In Repeat coding schemes, only the corresponding bits of BLOCKN[127:0] are useful. In different coding schemes, the values of useless register bits read by software are invalid.

The values of useful register bits read by software are the system parameters BLOCK1, BLOCK2, and BLOCK3 themselves instead of their values after being encoded.

Table Title: Table 5.3-5. Software Read Registers

Table:
| System Parameter | Bit Width | Bit | Name | Register |
|------------------|-----------|-----|------|---------|
| efuse_wr_disable | 16        | [15:0] | efuse | EFUSE_BLK0_RDATAO_REG |
| efuse_rd_disable | 4         | [3:0]   |       |         |
| flash_crypt_cnt | -         | [7:6:0]| flash | EFUSE_BLK0_RDATA1_REG |
| uart_download_dis | -    | [0]     |      |        |
| WIFI_MAC_Address | 56       | [31:0:55:32] | WIFI_MAC | EFUSE_BLK0_RDATA2_REG |
| disable_app_cpu | 1         | [0]     |      |        |
| disable_bt | 1         | [0]     |      |        |
| pkg_version | 4         | [3:0]   |       |        |
| disable_cache | 1         | [0]     |      |        |
| SPI_pad_config_hd | -    | [5:4:0]| SPI_pad | EFUSE_BLK0_RDATA3_REG |
| BLK3_part_reserve | -    | [0]     |      |        |
| CK8M_Frequency | 8         | [7:0]   |       |        |
| XPD_SDIO_REG | 1         | [0]     |       | EFUSE_BLK0_RDATA4_REG |
| SDIO_TIEH | 1         | [0]     |      |        |
| sdio_force | 1         | [0]     |      |        |
| SPI_pad_config_clk | -    | [5:4:0]| SPI_pad | EFUSE_BLK0_RDATA5_REG |
| SPI_pad_config_q | 5         | [4:0]   |       |        |
| SPI_pad_config_d | 5         | [4:0]   |       |        |
| SPI_pad_config_cs0 | -    | [4:0]| SPI_pad | EFUSE_BLK0_RDATA6_REG |
| vol_level_hp_inv | 2         | [1:0]   |       |        |
| dig_vol_l6 | 4         | [3:0]   |       |        |
| flash_crypt_config | -    | [3:0]| flash | EFUSE_BLK0_RDATA7_REG |
| coding_scheme | 2         | [1:0]   |       |        |
| console_debug_disable | -     | [0]      |       |        |
| abstract_done_0 | 1         | [0]     |       |        |
| abstract_done_1 | 1         | [0]     |       |        |

Footer:
Espressif Systems
98 ESP32 TRM (Version 5.6)
Submit Documentation Feedback

Navigation Link: GoBack