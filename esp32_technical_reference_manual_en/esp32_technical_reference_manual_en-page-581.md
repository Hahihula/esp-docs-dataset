**Title: Chapter 26 SDIO Slave Controller (SDIO)**

**GoBack**

**Register Section**
- **Register Name:** SLC_RX_DSCR_CONF_REG (0x98)
  - **Description:** 
    - `SLC_SLCO_TOKEN_NO_REPLACE`: Please initialize to 1. Do not modify it.
      - `(R/W)`
    - `SLCO_LEN_CONF_REG (0xE4)`
      - `SLCO_LEN_INC_MORE`
        - Set this bit to add the value of SLC0_LEN to that of SLC0_LEN_WDATA.

**Register Details**
- **Register Name:** SLCO_LEN
  - **Description:**
    - The packet length sent. `(WO)`
  
- **Register Name:** SLCO_LENGTH_REG (0xE8)
  - **Description:**
    - Indicates the packet length sent by the Slave. `(RO)`

**Section Title: SLC Host Registers**

**Body Text:**
The addresses in this section are relative to the SDIO Slave base address (0x3FF5_5000) provided in Table 3.3-6 in Chapter 3 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

**Footer Information:** 
- **Company Name:** Espressif Systems
- **Document Version:** ESP32 TRM (Version 5.6)
- **Page Number:** 581

**Link:**
- Submit Documentation Feedback