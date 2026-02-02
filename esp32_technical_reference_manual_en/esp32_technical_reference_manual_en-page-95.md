**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Section Header:**
Repeat

**Equation:**
`BLOCKN[255:128] = 'BLOCKN[127:0] = BLOCKN[127:0]`

**Subsection Titles and Content:**

- **5.3.1.4 BLK3_part_reserve**
  - System parameters coding_scheme, BLOCK1, BLOCK2, and BLOCK3 are controlled by the parameter `BLK3_part_reserve`.
  - When the value of `BLK3_part_reserve` is 0, coding_scheme, BLOCK1, BLOCK2, and BLOCK3 can be set to any value.
  - When the value of `BLK3_part_reserve` is 1, coding_scheme, BLOCK1, BLOCK2 are controlled by a specific scheme. Meanwhile, `BLOCK3[143:96]`, namely, `eBLOCK3[191:128]` is unavailable.

- **5.3.2 Programming of System Parameters**
  - The programming of variable-length system parameters BLOCK1, BLOCK2, and BLOCK3 differs from that for fixed-length system parameters.
  - We program the `eBLOCKN[255:0]` value on encoded system parameters BLOCK1, BLOCK2, and BLOCK3 instead directly programming these values. 
  - The bit width of `eBLOCKN[255:0]` is always set to be fixed-length (256 bits).
  - Fixed-length system parameters are programmed without encoding them first.
  
**Table Title:** Table 5.3-3. Program Registers

| Name                   | System parameter       | Bit     | Name                  | Register                | Bit |
|------------------------|------------------------|---------|-----------------------|-------------------------|-----|
| efuse_wr_disable       |                       | [16:0] | EFUSE_BLK0_WDATA0_REG |                        | [15:0] |
| efuse_rd_disable       |                       | [4]     |                       |                        | [19:16] |
| flash_crypt_cnt        |                       |         |                       |                        | [26:20] |
| uart_download_dis      |                       | [7]     |                       |                        | [6:0] |
| WiFi_MAC_Address       |                       | 56      |                       | EFUSE_BLK0_WDATA1_REG  | [31:0] |
| disable_app_cpu        |                       |         |                       | EFUSE_BLK0_WDATA2_REG  | [23:0] |
| disable_bt             |                       |         |                       |                        | [0] |
| pkg_version            |                       |         |                       |                        | [1] |
| disable_cache          |                       |         |                       | EFUSE_BLK0_WDATA3_REG  | [8:4] |
| SPI_pad_config_hd      |                       |         |                       |                        | [3] |
| BLK3_part_reserve     |                       |         |                       |                        | [14] |
| CK8M_Frequency         |                       |         |                       | EFUSE_BLK0_WDATA4_REG  | [7:0] |
| XPD_SDIO_REG           |                       |         |                       |                        | [15] |
| SDIO_TIEH              |                       |         |                       |                        | [16] |
| sdio_force             |                       |         |                       | EFUSE_BLK0_WDATA4_REG  | [9:5] |

**Footer Information:** 
Espressif Systems
EFUSE_BLK0_WDATA5_REG ESP32 TRM (Version 5.6)
Submit Documentation Feedback