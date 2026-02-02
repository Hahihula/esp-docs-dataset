**Title: Chapter 10 Timer Group (TIMG)**

---

### Register 10.11. TIMGn_WDTCONFIG1_REG (0x004c)

- **Description:** 
  - `TIMGn_WDT_CLK PRESCALE` MWDT clock prescale value.
  - `MWDT clock period = MWDTS clock source period * TIMGn_WDT_CLK PRESCALE.`

**Register Address:**
- `31`
- `0x00001`

---

### Register 10.12. TIMGn_WDTCONFIG2_REG (0x0050)

- **Description:** 
  - Stage O timeout value, in MWDT clock cycles.

**Register Address:**
- `31`
- `26000000`

---

### Register 10.13. TIMGn_WDTCONFIG3_REG (0x0054)

- **Description:** 
  - Stage 1 timeout value, in MWDT clock cycles.

**Register Address:**
- `31`
- `0x007FFFFF`

---

### Register 10.14. TIMGn_WDTCONFIG4_REG (0x0058)

- **Description:** 
  - Stage 2 timeout value, in MWDT clock cycles.

**Register Address:**
- `31`
- `0x000FFFFF`

---

### Register 10.15. TIMGn_WDTCONFIG5_REG (0x005c)

- **Description:** 
  - Stage 3 timeout value, in MWDT clock cycles.

**Register Address:**
- `31`
- `0x000FFFFF`

---

*Footer:*  
Espressif Systems  
Submit Documentation Feedback

*Page Number:* ESP32 TRM (Version 5.6) Page 230