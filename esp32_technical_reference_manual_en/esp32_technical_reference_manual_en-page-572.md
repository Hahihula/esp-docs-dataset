**Title: Chapter 26 SDIO Slave Controller (SDIO)**

---

### Table of Interrupt Registers and Their Descriptions:

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| SLCOHOST_CONF_W3_REG | Host and Slave communication register3 | 0x3FF55078 | R/W |
| SLCOHOST_CONF_W4_REG | Host and Slave communication register4 | 0x3FF5507C | R/W |
| SLCOHOST_CONF_W6_REG | Host and Slave communication register6 | 0x3FF55088 | R/W |
| SLCOHOST_CONF_W8_REG | Host and Slave communication register8 | 0x3FF5509C | R/W |
| SLCOHOST_CONF_W9_REG | Host and Slave communication register9 | 0x3FF550A0 | R/W |
| SLCOHOST_CONF_W10_REG | Host and Slave communication register10 | 0x3FF550A4 | R/W |
| SLCOHOST_CONF_W11_REG | Host and Slave communication register11 | 0x3FF550A8 | R/W |
| SLCOHOST_CONF_W12_REG | Host and Slave communication register12 | 0x3FF550AC | R/W |
| SLCOHOST_CONF_W13_REG | Host and Slave communication register13 | 0x3FF550B0 | R/W |
| SLCOHOST_CONF_W14_REG | Host and Slave communication register14 | 0x3FF550B4 | R/W |
| SLCOHOST_CONF_W15_REG | Host and Slave communication register15 | 0x3FF550B8 | R/W |
| SLCOHOST_CONF_REG | Edge configuration | 0x3FF551F0 | R/W |

---

### Interrupt Registers:

- **SLCOHOST_INT_RAW_REG**: Raw interrupt (Address: 0x3FF55000, Access: RO)
- **SLCOHOST_INT_ST_REG**: Masked interrupt status (Address: 0x3FF55058, Access: RO)
- **SLCOHOST_INT_CLR_REG**: Interrupt clear (Address: 0x3FF550D4, Access: WO)
- **SLCOHOST_FUNC1_INT_ENA_REG**: Interrupt enable (Address: 0x3FF550DC, Access: R/W)
- **SLCOHOST_CONF_W7_REG**: Interrupt vector for Host to interrupt Slave (Address: 0x3FF5508C, Access: WO)

---

### SDIO HINF registers:

| Name | Description | Address | Access |
|------|-------------|---------|--------|
| HINF_CFG_DATA1_REG | SDIO specification configuration | 0x3FF4B004 | R/W |

---

**Footer:**  
Espressif Systems  
572 ESP32 TRM (Version 5.6)  

[Submit Documentation Feedback](#)