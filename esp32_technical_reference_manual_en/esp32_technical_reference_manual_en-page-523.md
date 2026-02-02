**Title: Chapter 24 Ethernet Media Access Controller (EMAC)**

---

### Register 24.45, EMAC_EX_OSCCLK_CONF_REG (0x0804)

| Field | Name | Description |
|-------|------|-------------|
| 31    | reserved | Reserved for future use or specific implementation details. |
| 25-24 | EMAC OSC CLK SEL | Ethernet work using external PHY output clock or not for RMII CLK, when using RMII PHY. When this bit is set to 1, external PHY CLK is used. When this bit is set to 0, APLL CLK is used. (R/W) |
| 18-17 | EMAC OSC H DIV NUM 100M | RMII/MII half-integer divider when register EMAC OSC H clock divider’s speed is 100M. (R/W) |
| 12-11 | EMAC OSC DIV NUM 100M | whole-integer divider, when register EMAC EX CLK OUT CONF clock divider's speed is 100M. (R/W) |
| 6-5   | EMAC OSC H DIV NUM 100M | half-integer divider, when register EMAC EX CLK OUT CONF clock divider’s speed is 100M. (R/W) |
| 4     | EMAC OSC DIV NUM 10M | whole-integer divider, when register EMAC EX CLK OUT CONF clock divider's speed is 10M. (R/W) |

---

### Register 24.46, EMAC_EX_CLK_CTRL_REG (0x0808)

| Field | Name | Description |
|-------|------|-------------|
| 31    | reserved | Reserved for future use or specific implementation details. |
| 30-29 | EMAC_MII_CLK_RX_EN | Enable Ethernet RX CLK. (R/W) |
| 28-27 | EMAC_MII_CLK_TX_EN | Enable Ethernet TX CLK. (R/W) |
| 26    | EMAC_INT_OSC_EN | Using internal APLL CLK in RMII PHY mode. (R/W) |
| 25    | EMAC_EXT_OSC_EN | Using external APLL CLK in RMII PHY mode. (R/W) |

---

**Footer:**
- Page number: 523
- Document version: ESP32 TRM (Version 5.6)
- Company name: Espressif Systems

[Submit Documentation Feedback](#)