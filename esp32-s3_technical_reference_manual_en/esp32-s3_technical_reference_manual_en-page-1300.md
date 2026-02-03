**Chapter Title:**
Chapter 34 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

**Register Description and Details for Register 34.27, SDHOST_HCON_REG (0x0070):**

- **Field Descriptions with Bit Positions in Hexadecimal Notation:**
  - `0x0` to `0x1`: Reserved
  - `0x2`: SDHOST_NUM_CLK_DIV_REG Have 4 clk divider in design. (RO)
  - `0x3`: SDHOST_HOLD_REG Have a hold register in data path . (RO)
  - `0x4`: SDHOST_RAM_INDISE_REG Inside RAM in SDMMC module. (RO)
  - `0x5`: SDHOST_DMA_WIDTH_REG DMA data width is 32. (RO)
  - `0x6`: SDHOST_ADDR_WIDTH_REG Register address width is 32. (RO)
  - `0x7`: SDHOST_DATA_WIDTH_REG Register data width is 32. (RO)
  - `0x8`: SDHOST_BUS_TYPE_REG Register config is APB bus. (RO)
  - `0x9`: SDHOST_CARD_NUM_REG Support card number is 2. (RO)
  - `0xA`: SDHOST_CARD_TYPE_REG Hardware support SDIO and MMC. (RO)

**Register Description for Register 34.28, SDHOST_UHS_REG (0x0074):**

- **Field Descriptions with Bit Positions in Hexadecimal Notation:**
  - `0x0` to `0x1`: Reserved
  - `0x2`: SDHOST_DDR_REG DDR mode selecton,1 bit for each card. (R/W)
    - `0`: Non-DDR mdoe.
    - `1`: DDR mdoe.

---

**Footer:**
Espressif Systems  
Submit Documentation Feedback

**Document Version:** ESP32-S3 TRM (Version 1.7)