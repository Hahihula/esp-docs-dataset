**Title:**
Chapter 5 eFuse Controller (EFUSE)

**Menu:**
GoBack

**Register Information Title:**
Register 5.6. EFUSE_BLK0_RDATA5_REG (0x014)

**Binary Diagram Description:**
A binary diagram showing the layout of register bits from bit 31 to bit 0.

**Field Descriptions and Values in Markdown Format:**

- **EFUSE_RD_FLASH_CRYPT_CONFIG**: This field returns the value of flash_crypt_config. (RO)
  
- **EFUSE_RD_DIG_VOL_L6**: This field stores the difference between the digital regulator voltage at level 6 and 1.2 V. (RO)

- **EFUSE_RD_VOL_LEVEL_HP_INV**: This field stores the voltage level for CPU to run at 240 MHz, or for flash/PSRAM to run at 80 MHz. 0x0: level 7; 0x1: level 6; 0x2: level 5; 0x3: level 4. (RO)

- **EFUSE_RD_SPI_PAD_CONFIG_CS0**: This field returns the value of SPI_pad_config_cs0. (RO)

- **EFUSE_RD_SPI_PAD_CONFIG_D**: This field returns the value of SPI_pad_config_d. (RO)

- **EFUSE_RD_SPI_PAD_CONFIG_Q**: This field returns the value of SPI_pad_config_q. (RO)

- **EFUSE_RD_SPI_PAD_CONFIG_CLK**: This field returns the value of SPI_pad_config_clk. (RO)

**Footer:**
Espressif Systems
ESP32 TRM (Version 5.6)
Submit Documentation Feedback