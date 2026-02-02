**Chapter Title:**
Chapter 5 eFuse Controller (EFUSE)

**Section Header:**
Register 5.4. EFUSE_BLK0_RDATA3_REG (0x0c)

**Binary Register Diagram Description:**
- The diagram shows a binary register with various fields labeled, such as "EFUSE_RD_CHIP_VER_PKG" and others.
- Each field is numbered from left to right.

**Field Descriptions for 5.4 EFUSE_BLK0_RDATA3_REG (0x0c):**

1. **EFUSE_RD_CHIP_VER_PKG**
   - Description: These are the first three identification bits of chip packaging version among the four identification bits.
   - Access Type: Read Only

2. **EFUSE_RD_SPI_PAD_CONFIG_HD**
   - Description: This field returns the value of SPI_pad_config_hd.
   - Access Type: Read Only

3. **EFUSE_RD_CHIP_VER_DIS_CACHE**
   - Description: Disables cache.
   - Access Type: Read Only

4. **EFUSE_RD_CHIP_VER_PKG**
   - Description: This is the fourth identification bit of chip packaging version among the four identification bits.

**Section Header:**
Register 5.5. EFUSE_BLK0_RDATA4_REG (0x10)

**Binary Register Diagram Description for 5.5 EFUSE_BLK0_RDATA4_REG (0x10):**
- The diagram shows a binary register with various fields labeled, such as "EFUSE_RD_SDIO_FORCE" and others.
- Each field is numbered from left to right.

**Field Descriptions for 5.5 EFUSE_BLK0_RDATA4_REG (0x10):**

1. **EFUSE_RD_SDIO FORCE**
   - Description: This field returns the value of sdio_force.
   - Access Type: Read Only

2. **EFUSE_RD_SDIO TIEH**
   - Description: This field returns the value of SDIO_TIEH.
   - Access Type: Read Only

3. **EFUSE_RD_XPD_SDIO**
   - Description: This field returns the value of XPD_SDIO_REG.
   - Access Type: Read Only

4. **ESFUSE_RD_CK8M_FREQ**
   - Description: RC_FAST_CLK frequency.
   - Access Type: Read Only

**Footer Information:**
- Page number 104
- Document version ESP32 TRM (Version 5.6)
- Company name Espressif Systems
- Link to Submit Documentation Feedback