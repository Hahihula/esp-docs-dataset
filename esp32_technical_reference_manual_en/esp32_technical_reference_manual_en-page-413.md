**Chapter Title:**
Chapter 21 I2C Controller (I2C)

**Section Header:**
GoBack

**Register Information and Description:**

- **Register Name:** Register 21.18, I2C_SCL_STOP_SETUP_REG (0x004C)
  - **Description:** This register is used to configure the time between the positive edge of SCL and the positive edge of SDA, in APB clock cycles.
  - **Access Type:** Read/Write
  - **Bit Description:**
    - **I2C_SCL_STOP_SETUP_TIME** (0x004C)
      - **Description:** This register is used to configure the time between the positive edge of SCL and the positive edge of SDA, in APB clock cycles.
      - **Access Type:** Read/Write
  - **Bit Layout:**
    - **Reset Value:** All bits are set to '0'.

- **Register Name:** Register 21.19, I2C_SCL_FILTER_CFG_REG (0x050)
  - **Description:** This is the filter enable bit for SCL.
  - **Access Type:** Read/Write
  - **Bit Description:**
    - **I2C_SCL_FILTER_EN** 
      - **Description:** When a pulse on the SCL input has smaller width than this register value in APB clock cycles, the I2C controller will ignore that pulse. (R/W)
  - **Bit Layout:**
    - **Reset Value:** All bits are set to '0'.

- **Register Name:** Register 21.20, I2C_SDA_FILTER_CFG_REG (0x054)
  - **Description:** This is the filter enable bit for SDA.
  - **Access Type:** Read/Write
  - **Bit Description:**
    - **I2C_SDA_FILTER_EN** 
      - **Description:** When a pulse on the SDA input has smaller width than this register value in APB clock cycles, the I2C controller will ignore that pulse. (R/W)
  - **Bit Layout:**
    - **Reset Value:** All bits are set to '0'.

**Footer Information:**
- Page Number: 413
- Document Title: ESP32 TRM (Version 5.6)
- Company Name: Espressif Systems

**Action Links:**
- Submit Documentation Feedback