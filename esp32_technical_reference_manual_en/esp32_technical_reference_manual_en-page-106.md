**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Section Header:**
Register 5.7. EFUSE_BLK0_RDATA6_REG (0x018)

**Binary Register Diagram Description:**
- The diagram shows a binary register with labels for each bit position from right to left.
- Labels include:
  - EFUSE_RD_KEY_STATUS
  - EFUSE_RD_DISABLE_DL_CACHE
  - EFUSE_RD_DISABLE_DL_DECRYPT
  - EFUSE_RD_DISABLE_DL_ENCRYPT
  - EFUSE_RD_DISABLE_JTAG
  - EFUSE_RD_ABS_DONE_1
  - EFUSE_RD_ABS_DONE_0
  - EFUSE_RD_CONSOLE_DEBUG_DISABLE
  - EFUSE_RD_CODING_SCHEME

**Field Descriptions:**
- **EFUSE_RD_KEY_STATUS:** This field returns the value of key_status. (RO)
- **EFUSE_RD_DISABLE_DL_CACHE:** This field returns the value of download_dis_cache. (RO)
- **EFUSE_RD_DISABLE_DL_DECRYPT:** This field returns the value of download_dis_decrypt. (RO)
- **EFUSE_RD_DISABLE_DL_ENCRYPT:** This field returns the value of download_dis_encrypt. (RO)
- **EFUSE_RD_DISABLE_JTAG:** This field returns the value of JTAG_disable. (RO)
- **EFUSE_RD_ABS_DONE_1:** This field returns the value of abstract_done_1. (RO)
- **EFUSE_RD_ABSDone_0:** This field returns the value of abstract_done_0. (RO)
- **EFUSE_RD_CONSOLE_DEBUG_DISABLE:** This field returns the value of console_debug_disable. (RO)
- **EFUSE_RD_CODING_SCHEME:** This field returns the value of coding_scheme. (RO)

**Section Header:**
Register 5.8. EFUSE_BLK0_WDATA0_REG (0x01c)

**Binary Register Diagram Description:**
- The diagram shows a binary register with labels for each bit position from right to left.
- Labels include:
  - EFUSE_UART_FLASHHCRYPT_CNT
  - EFUSE_RD_WRDis
  - EFUSE_WRDis

**Field Descriptions:**
- **EFUSE_UART_DOWNLOAD_DIS:** This bit programs the value of uart_download_dis. Valid only for ESP32 ECO V3. (R/W)
- **EFUSE_FLASHCRYPT_CNT:** This field programs the value of flash_crypt_cnt. (R/W)
- **EFUSE_RDDis:** This field programs the value of efuse_rd_disable. (R/W)
- **EFUSE_WRDis:** This field programs the value of efuse_wr_disable. (R/W)

**Footer:**
Espressif Systems
Submit Documentation Feedback

**Document Information:**
ESP32 TRM (Version 5.6)