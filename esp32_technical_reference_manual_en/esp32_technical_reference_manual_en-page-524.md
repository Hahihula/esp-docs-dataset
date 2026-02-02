**Title:**
Chapter 24 Ethernet Media Access Controller (EMAC)

**Subtitles and Sections with Descriptions:**

1. **Register 24.47, EMAC_EX_PHYINF_CONF_REG (0x80C)**
   - Description:
     - `EMAC_PHY_INTF_SEL` The PHY interface selected.
     - Values provided in a binary format.

2. **Register 24.48, EMAC_PD_SEL_REG (0x810)**
   - Description: 
     - `EMAC_RAM_PD_EN` Ethernet RAM power-down enable signal.
     - Bit[0]: TX SRAM; Bit[1]: RX SRAM
     - Setting the bit to 1 powers down the RAM.

**Footer Information:**
- Page number and document version:
  - "524 ESP32 TRM (Version 5.6)"
  
- Company information:
  - Espressif Systems

- Navigation links:
  - GoBack
  
- Feedback link:
  - Submit Documentation Feedback