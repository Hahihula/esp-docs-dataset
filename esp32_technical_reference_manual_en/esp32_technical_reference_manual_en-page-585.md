**Chapter Title:**
Chapter 26 SDIO Slave Controller (SDIO)

**GoBack Link:** GoBack

---

### Register Section:

#### **Register 26.17, SLCHOST_PKT_LEN_REG (0x6D)**
- Diagram:
  - `SLCHOST_HOSTREG_SLCO_LEN_CHECK`
    - Bits: [31, 20, 19, 0]
    - Value: `0x000` to `0x000`

**Description for SLCHOST_HOSTREG_SLCO_LEN_CHECK**
- **Text:** Its value is HOSTREG_SLCO_LEN[9:0] plus HOSTREG_SLCO_LEN[19:10]. (RO)
- **Additional Information:** 
  - Description:
    - `SLCHOST_HOSTREG_SLCO_LEN`: The accumulated value of the data length sent by the Slave. The value gets updated only when the Host reads it.

#### **Register 26.18, SLCHOST_CONF_WO_REG (0x6C)**
- Diagram: 
  - `SLCHOST_CONF3`, `SLCHOST_CONF2`, `SLCHOST_CONF1`, and `SLCHOST_CONFO`
    - Bits: [31, 24, 16, 8, 7, 0]
    - Value: `0x000` to `0x000`

**Description for SLCHOST_CONF3**
- **Text:** The information interaction register between Host and Slave. Both Host and Slave can access it. (R/W)

**Description for SLCHOST_CONF2**
- **Text:** The information interaction register between Host and Slave. Both Host and Slave can access it. (R/W)

**Description for SLCHOST_CONF1**
- **Text:** The information interaction register between Host and Slave. Both Host and Slave can access it. (R/W)

**Description for SLCHOST_CONFO**
- **Text:** The information interaction register between Host and Slave. Both Host and Slave can access it. (R/W)

---

**Footer:**
Espressif Systems
Page Number 585 ESP32 TRM (Version 5.6)
Submit Documentation Feedback