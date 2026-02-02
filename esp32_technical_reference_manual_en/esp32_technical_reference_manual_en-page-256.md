**Chapter Title:**
Chapter 12 DPort Registers

**GoBack Link:** GoBack

---

**Section Header (Register):**
Register 12.19. DPORT_PERIP_CLK_EN_REG (0xCO)

**Body Text and Descriptions for Register 12.19:**
Continued from the previous page...

- **DPORUART1_CLK_EN**: UART1 module. (R/W)
- **DPORT2SO_CLK_EN**: I2S0 module. (R/W)
- **DPORT_UART_CLK_EN**: UARTO module. (R/W)
- **DPORT_SPI01_CLK_EN**: SPI0 and SPI1 module. (R/W)

**Section Header:**
Register 12.20. DPORT_PERIP_RST_EN_REG (0xC4)

**Body Text for Register 12.20 Description:**
Set each bit to reset the corresponding module. Clear the bit to release the corresponding module.

For a list of modules, please refer to register 12.19.
- **Bit Positions and Labels**: 
  - The image shows various bits labeled from RST to DPORT_UART1to DPORT_SPI01, with some reserved positions marked as (reserved).

**Section Header:**
Register 12.21. DPORT_WIFI_CLK_EN_REG (0xCC)

**Body Text for Register 12.21 Description:**
Set the bit to enable the clock of Ethernet MAC module.

- **DPORT_WIFI_CLK_EMAC_EN**: Set the bit to disable the clock of Ethernet MAC module.
- Clear the bit

- **DPORT_WIFI_CLK_SDIO_HOST_EN**: Set the bit to enable the clock of SD/MMC module. 

- **DPORT_WIFI_CLK_SDIOSLAVE_EN**: Set the bit to clear.

**Additional Information:**
To disable the clock, refer to register 12.19.
- (R/W) indicates read/write access for each setting in registers described above

---

**Footer:**
Espressif Systems
Submit Documentation Feedback ESP32 TRM (Version 5.6)
Page number at bottom center of page is "256"