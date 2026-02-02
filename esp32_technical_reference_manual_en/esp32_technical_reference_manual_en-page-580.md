**Title: Chapter 26 SDIO Slave Controller (SDIO)**

---

### Register 26.9, SLCOTOKEN1_REG (0x54)

| Field | Value |
|-------|-------|
| 31    | reserved |
| 28    | 0      |
| 27    | 0      |
| ...   | ...    |
| 0     | 0      |

**Description:**
- **SLCOTOKEN1_SLCO_TOKEN1**: The accumulated number of buffers for receiving packets. (RO)
- **SLCOTOKEN1_SLCO_TOKEN1_INC_MORE**: Set this bit to add the value of SLCOTOKEN1_SLCO_TOKEN1_WDATA to that of SLCOTOKEN1_SLCO_TOKEN1 (WO).
- **SLCOTOKEN1_SLCO_TOKEN1_WDATA**: The number of available receiving buffers. (WO)

---

### Register 26.10, SLCCONF1_REG (0x60)

| Field | Value |
|-------|-------|
| 31    | reserved |
| 28    | ...     |
| 27    | ...     |
| ...   | ...     |
| 0     | 0      |

**Description:**
- **SLCCONF1_SLCO_RX_STITCH_EN**: Please initialize to O. Do not modify it. (R/W)
- **SLCCONF1_SLCO_TX_STITCH_EN**: Please initialize to O. Do not modify it. (R/W)
- **SLCCONF1_SLCO_LEN_AUTO_CLR**: Please initialize to 0. Do not modify it. (R/W)

---

**Footer:**
Espressif Systems  
ESP32 TRM (Version 5.6)  
Submit Documentation Feedback