**Chapter Title:**
Chapter 27 I2C Controller (I2C)

**GoBack Link:** GoBack

---

**Section Header: Register 27.4, I2C_SCL_HIGH_PERIOD_REG (0x038)**

- **Field Description for I2C_SCL_HIGH_PERIOD:**
  - **Text:** "This field is used to configure how long SCL remains high in master mode, in I2C module clock cycles."
  - **Access Type:** Read/Write
  - **Bit Positions:** Not specified (but implied by the diagram)

- **Field Description for I2C_SCL_WAIT_HIGH_PERIOD:**
  - **Text:** "This field is used to configure the SCL FSM’s waiting period for SCL high level in master mode, in I2C module clock cycles."
  - **Access Type:** Read/Write
  - **Bit Positions:** Not specified (but implied by the diagram)

---

**Section Header: Register 27.5, I2C_SCL_START_HOLD_REG (0x040)**

- **Field Description for I2C_SCL_START_HOLD_TIME:**
  - **Text:** "This field is used to configure the time between the falling edge of SDA and the falling edge of SCL for a START condition in I2C module clock cycles."
  - **Access Type:** Read/Write
  - **Bit Positions:** Not specified (but implied by the diagram)

---

**Section Header: Register 27.6, I2C_SCL_RSTART_SETUP_REG (0x044)**

- **Field Description for I2C_SCL_RSTART_SETUP_TIME:**
  - **Text:** "This field is used to configure the time between the rising edge of SCL and the falling edge of SDA for a RSTART condition in I2C module clock cycles."
  - **Access Type:** Read/Write
  - **Bit Positions:** Not specified (but implied by the diagram)

---

**Footer:**
- "Espressif Systems"
- Page Number: 1019
- Document Title: ESP32-S3 TRM (Version 1.7)
- Link Texts:
  - Submit Documentation Feedback