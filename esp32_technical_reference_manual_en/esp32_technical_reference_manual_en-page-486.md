**Chapter 24: Ethernet Media Access Controller (EMAC)**

---

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| EMACADDR1HIGH_REG | MAC address filtering and upper 16 bits of the second 6-byte MAC address | 0x3FF6A048 | R/W |
| EMACADDR1LOW_REG | Lower 32 bits of the second 6-byte MAC address | 0x3FF6A04C | R/W |
| EMACADDR2HIGH_REG | MAC address filtering and upper 16 bits of the third 6-byte MAC address | 0x3FF6A050 | R/W |
| EMACADDR2LOW_REG | Lower 32 bits of the third 6-byte MAC address | 0x3FF6A054 | R/W |
| EMACADDR3HIGH_REG | MAC address filtering and upper 16 bits of the fourth 6-byte MAC address | 0x3FF6A058 | R/W |
| EMACADDR3LOW_REG | Lower 32 bits of the fourth 6-byte MAC address | 0x3FF6A05C | R/W |
| EMACADDR4HIGH_REG | MAC address filtering and upper 16 bits of the fifth 6-byte MAC address | 0x3FF6A060 | R/W |
| EMACADDR4LOW_REG | Lower 32 bits of the fifth 6-byte MAC address | 0x3FF6A064 | R/W |
| EMACADDR5HIGH_REG | MAC address filtering and upper 16 bits of the sixth 6-byte MAC address | 0x3FF6A068 | R/W |
| EMACADDR5LOW_REG | Lower 32 bits of the sixth 6-byte MAC address | 0x3FF6A06C | R/W |
| EMACADDR6HIGH_REG | MAC address filtering and upper 16 bits of the seventh 6-byte MAC address | 0x3FF6A070 | R/W |
| EMACADDR6LOW_REG | Lower 32 bits of the seventh 6-byte MAC address | 0x3FF6A074 | R/W |
| EMACADDR7HIGH_REG | MAC address filtering and upper 16 bits of the eighth 6-byte MAC address | 0x3FF6A078 | R/W |
| EMACADDR7LOW_REG | Lower 32 bits of the eighth 6-byte MAC address | 0x3FF6A07C | R/W |
| EMACWDGTO_REG | Watchdog timeout control | 0x3FF6A0DC | R/W |

**Clock configuration registers**

- **EMAC_EX_CLKOUT_CONF_REG**: RMII clock divider setting
- **EMACEx OSCCLKConf Reg**: RMII clock half and whole divider settings

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| EMACEx CLKCTRLReg | Clock enable and external / internal clock selection | 0x3FF69804 | R/W |

**PHY type and SRAM configuration registers**

- **EMACEx PHYINFConf Reg**: Selection of MII / RMII phy
- **EMACPDSELReg**: Ethernet RAM power-down enable

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| EMACEx PHYINFConf Reg | Selection of MII / RMII phy | 0x3FF6980C | R/W |
| EMACPDSELReg | Ethernet RAM power-down enable | 0x3FF69810 | R/W |

---

**24.10 Registers**

The addresses in this section are relative to the EMAC base address provided in Table 3.3-6 in Chapter 3 System and Memory. The absolute register addresses are listed in Section **24.9 Register Summary**.

Espressif Systems  
ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)