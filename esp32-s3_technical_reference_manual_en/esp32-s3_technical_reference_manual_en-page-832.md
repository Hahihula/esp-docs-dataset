**Title:**
Chapter 17 System Registers (SYSTEM)

**Subtitle:**
Register 17.5. SYSTEM_PERIP_CLK_EN1_REG (0x001C)

**Menu/Table of Contents:**
- SYSTEM_USB_DEVICE_CLK_EN
- SYSTEM_SDIO_HOST_CLK_EN
- SYSTEM_LCD_CAM_CLK_EN
- SYSTEM_UART2_CLK_EN
- SYSTEM_USB_DEVICE_CLK_EN

**Body Text with Descriptions and Register Information for Each Field in SYSTEM_PERIP_CLK_EN1_REG (0x001C):**

- **[Field 31] (reserved)**
  
- **[Fields from bit 1 to bit 0, each corresponding to a specific clock enablement option]:**
  - SYSTEM_PERI_BACKUP_CLK_EN: Set this bit to enable peri backup clock. (R/W)
  - SYSTEM_CRYPTO_AES_CLK_EN: Set this bit to enable AES clock. (R/W)
  - SYSTEM_CRYPTO_SHA_CLK_EN: Set this bit to enable SHA clock. (R/W)
  - SYSTEM_CRYPTO_RSA_CLK_EN: Set this bit to enable RSA clock. (R/W)
  - SYSTEM_CRYPTO_DS_CLK_EN: Set this bit to enable DS clock. (R/W)
  - SYSTEM_CRYPTO_HMAC_CLK_EN: Set this bit to enable HMAC clock. (R/W)
  - SYSTEM_DMA_CLK_EN: Set this bit to enable DMA clock. (R/W)
  - SYSTEM_SDIO_HOST_CLK_EN: Set this bit to enable SDIO_HOST clock. (R/W)
  - SYSTEM_LCD_CAM_CLK_EN: Set this bit to enable LCD_CAM clock. (R/W)
  - SYSTEM_UART2_CLK_EN: Set this bit to enable UART2 clock. (R/W)

**Footer Information:**
- Page number and document version:
  - "832 ESP32-S3 TRM (Version 1.7)"
  
- Company information:
  - Espressif Systems

- Link for submitting documentation feedback:
  - Submit Documentation Feedback