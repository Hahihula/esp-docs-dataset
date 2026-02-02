**Title: Chapter 5 eFuse Controller (EFUSE)**

---

### Register 5.12. EFUSE_BLK0_WDATA4_REG (0x02c)

| Bit Position | Name                          |
|--------------|-------------------------------|
| 31           | reserved                      |
| ...          | ...                           |
| 8            | reserved                      |
| 7            | EFUSE_SDIO_FORCE              |
| 6            | EFUSE_SDIO_TIEH               |
| 5            | EFUSE_XPD_SDIO                |
| 4            | EFUSE_CK8M_FREQ               |
| ...          | ...                           |
| 0            | Reset                         |

- **EFUSE_SDIO FORCE**: This field programs the value of SDIO_TIEH. (R/W)
  
- **EFUSE_SDIO TIEH**: This field programs the value of SDIO_TIEH. (R/W)

- **EFUSE_XPD_SDIO**: This field programs the value of XPD_SDIO_REG. (R/W)

- **EFUSE_CK8M_FREQ**: This fields program the frequency of RC_FAST_CLK. (R/W)

---

### Register 5.13. EFUSE_BLK0_WDATA5_REG (0x030)

| Bit Position | Name                          |
|--------------|-------------------------------|
| 31           | reserved                      |
| ...          | ...                           |
| 8            | reserved                      |
| 7            | EFUSE_FLASHCRYPT_CONFIG       |
| 6            | EFUSE_DIG_VOL_L6              |
| 5            | EFUSE_VOL_LEVEL_HP INV        |
| 4            | EFUSE_SPI_PAD_CONFIG_CS0      |
| 3            | EFUSE_SPI_PAD_CONFIG_D        |
| ...          | ...                           |
| 0            | Reset                         |

- **EFUSE_FLASHCRYPT_CONFIG**: This field programs the value of flash_crypt_config. (R/W)

- **EFUSE_DIG_VOL_L6**: This field stores the difference between the digital regulator voltage at level 6 and 1.2 V. (R/W)

- **EFUSE_VOL_LEVEL_HP INV**: These bits store the voltage level for CPU to run at 240 MHz, or for flash/PSRAM to run at 80 MHz. 0x0: level 7; 0x1: level 6; 0x2: level 5; 0x3: level 4. (R/W)

- **EFUSE_SPI_PAD_CONFIG_CS0**: This field programs the value of SPI_pad_config_cs0. (R/W)

- **EFUSE_SPI_PAD_CONFIG_D**: This field programs the value of SPI_pad_config_d. (R/W)

- **EFUSE_SPI_PAD_CONFIG_Q**: This field programs the value of SPI_pad_config_q. (R/W)

- **EFUSE_SPI_PAD_CONFIG_CLK**: This field programs the value of SPI_pad_config_clk. (R/W)

---

**Footer:**
Espressif Systems
108 ESP32 TRM (Version 5.6)
Submit Documentation Feedback