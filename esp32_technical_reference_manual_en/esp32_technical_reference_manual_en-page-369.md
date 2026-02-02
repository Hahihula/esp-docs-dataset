**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Register Information:**
- Register Name: SPI_CTRL2_REG (0x14)
- Table Description:
  - **Columns:** SPI_CS_DELAY_NUM, SPI_CS_DELAY_MODE, SPI_MOSI_DELAY_NUM, SPI_MISO_DELAY_NUM, reserved, SPI_HOLD_TIME, SPI_SETUP_TIME
  - **Rows:** Values in hexadecimal format for each column

**Field Descriptions:**

1. **SPI_CS_DELAY_NUM**
   - Reserved.

2. **SPI_CS_DELAY_MODE**
   - Reserved.

3. **SPI_MOSI_DELAY_NUM**
   - Description:
     - Used to configure the number of system clock cycles by which the MOSI signals are delayed.
     - Access Mode (R/W)
   - Details: 
     - This register field determines how SPI clock delay is managed for MOSI signals based on configuration in `SPI_MOSI_DELAY_MODE`.
     - Possible values:
       1. If SPI_CK_OUT_EDGE or SPI_CK_I_EDGE is set, the MOSI signals are delayed by half a cycle.
       2. If SPI_CK_OUT_EDGE or SPI_CK_I_EDGE is not set (default), the MOSI signals will be delayed one clock cycle.

4. **SPI_MOSI_DELAY_MODE**
   - Description:
     - This register field determines how the delay of MOSI signal by `SPI_MOSI_DELAY_NUM` system clocks should occur.
     - Access Mode (R/W)
   - Details: 
     1. If SPI_CK_OUT_EDGE or SPI_CK_I_EDGE is set, MISO signals are delayed half a cycle after being configured in this field; otherwise one clock cycle delay occurs by default.

5. **SPI_MISO_DELAY_NUM**
   - Description:
     - Used to configure the number of system clock cycles for which MOSI signal delays occur.
     - Access Mode (R/W)
   - Details: 
     1. After being delayed, MISO signals are de-registered based on configuration in `SPI_MOSI_DELAY_MODE`.

6. **SPI_MISO_DELAY_MODE**
   - Description:
     - This register field determines how the delay of MOSI signal by `SPI_MISO_DELAY_NUM` system clocks should occur.
     - Access Mode (R/W)
   - Details: 
     1. If SPI_CK_OUT_EDGE or SPI_CK_I_EDGE is set, MISO signals are delayed half a cycle after being configured in this field; otherwise one clock cycle delay occurs by default.

7. **SPI_HOLD_TIME**
   - Description:
     - The number of SPI clock cycles during which CS pin signals remain valid.
     - Access Mode (R/W)
     - Valid when `SPI_CS HOLD` is set to 1

8. **SPI_SETUP_TIME**
   - Description:
     - Configures the time between the CS signal active edge and first SPI clock edge in half-duplex mode or QSPI mode, with `SPI_CS SETUP` valid.
     - Access Mode (R/W)

**Footer:**
- Company Name: Espressif Systems
- Document Title: ESP32 TRM (Version 5.6)
- Page Number: 369

**Action Links:**
- Submit Documentation Feedback