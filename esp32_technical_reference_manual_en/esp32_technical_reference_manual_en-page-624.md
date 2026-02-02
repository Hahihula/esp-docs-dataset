**Chapter Title:**
Chapter 27 SD/MMC Host Controller (SDHOST)

**GoBack Link:** GoBack

---

### Register Section:

- **Register Name and Address:**
  - **Register 27.24. DEBNCE_REG (0x0064)**
    - **DEBOUNCE_COUNT**: Number of host clocks (clk) used by debounce filter logic.
      - The typical debounce time is 5 ~ 25 ms to prevent the card instability when the card is inserted or removed.

- **Register Name and Address:**
  - **Register 27.25. USRID_REG (0x0068)**
    - **USRID_REG**: User identification register, value set by user.
      - Default reset value can be picked by user while configuring core before synthesis.
      - Can also be used as a scratchpad register by user.

- **Register Name and Address:**
  - **Register 27.26. RST_N_REG (0x0078)**
    - **RST_CARD_RESET**: Hardware reset.
      - Active mode; O: Reset
      - These bits cause the cards to enter pre-idle state, which requires them to be re-initialized.

---

**Footer Information:**  
Espressif Systems  
Page Number and Document Version:
- Page 624 of ESP32 TRM (Version 5.6)  

**Feedback Link:**
Submit Documentation Feedback