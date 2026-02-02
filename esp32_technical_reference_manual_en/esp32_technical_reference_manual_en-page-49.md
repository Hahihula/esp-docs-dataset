**Chapter Title:**
Chapter 1 ULP Coprocessor (ULP)

**Section Header:**
Register 1.6. SENS_SAR_SLAVE_ADDR4_REG (0x0048)

**Table Description for Register 1.6:**
- **Columns:** Bits, Name of the bits
- **Rows:**
  - `31` to `29`: SENS_I2C_DONE
    - Description: Indicate I2C done.
    - Access Mode (RO)
  - `22`: SENS_I2C_RDATA
    - Description: I2C read data.
    - Access Mode (RO)
  - `11` to `0`: SENS_I2C_SLAVE_ADDR6, SENS_I2C_SLAVE_ADDR7
    - Description:
      - SENS_I2C_SLAVE_ADDR6: I2C slave address 6. (R/W)
      - SENS_I2C_SLAVE_ADDR7: I2C slave address 7. (R/W)

**Section Header:**
Register 1.7. SENS_SAR_I2C_CTRL_REG (0x0050)

**Table Description for Register 1.7:**
- **Columns:** Bits, Name of the bits
- **Rows:**
  - `31` to `28`: SENS_SAR_I2C_START FORCE, SENS_SAR_I2C_START
    - Description:
      - SENS_SAR_I2C_START FORCE: I2C started by SW. (R/W)
      - SENS_SAR_I2C_START: Start I2C; active only when SENS_SAR_I2C_START FORCE = 1.
- `0`: SENS_SAR_I2C_CTRL
    - Description:
      - SENS_SAR_I2C_CTRL: I2C control data. (R/W)

**Subsection Title and Content:**
1.8.2 RTC_I2C Address Space

**Body Text for Subsection 1.8.2:**
The addresses in parenthesis besides register names are the register addresses relative to (the RTC base address + 0x0C00). The RTC base address is provided in Table 3.3-6 Peripheral Address Mapping in Chapter 3 System and Memory. The absolute register addresses are listed in Section 17.2 RTC_I2C Address Space.

**Footer:**
Espressif Systems
49 ESP32 TRM (Version 5.6)
Submit Documentation Feedback