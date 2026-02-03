**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Section Header:**
Register 30.4. SPI_USER1_REG (0x0014)

**Table Description and Values for Register 30.4:**

- **SPI_USR_ADDR_BITLEN**: 
  - Value Range: [27, 26, 25, 24, 23]
  - Default Value: 0x1
  - Description:
    - The length of DUMMY state in unit of SPI_CLK cycles.
    - The value is (the expected cycle number - 1).
    - Can be configured in CONF state. (R/W)

- **SPI_CS_HOLD_TIME**:
  - Value Range: [27, 26, 25, 24, 23]
  - Default Value: 0
  - Description:
    - Delay cycles of CS pin.
    - In units of SPI_CLK cycles.
    - This field is used together with SPI_CS_HOLD.
    - Can be configured in CONF state. (R/W)

- **SPI_USR_DUMMY_CYCLELEN**:
  - Value Range: [27, 26, 25, 24, 23]
  - Default Value: 0
  - Description:
    - The length of DUMMY state.
    - In unit of SPI_CLK cycles.

- **SPI_MST_WFULL_ERR_EN**:
  - Value Range: [17, 16, 15, 14, 13]
  - Default Value: 0
  - Description:
    - SPI transfer is ended when SPI RX AFIFO wfull error occurs in GP-SPI master full-/half-duplex modes.
    - 0: SPI transfer is not ended when SPI RX AFIFO wfull error occurs in GP-SPI master full-/half-duplex modes. (R/W)

- **SPI_CS_SETUP_TIME**:
  - Value Range: [17, 16, 15, 14, 13]
  - Default Value: 0
  - Description:
    - The length of prepare (PREP) state.
    - In unit of SPI_CLK cycles.
    - This value is equal to the expected cycles -1.

- **SPI_CS_HOLD_TIME**:
  - Value Range: [27, 26, 25, 24, 23]
  - Default Value: 0
  - Description:
    - Delay cycles of CS pin.
    - In units of SPI_CLK cycles.
    - This field is used together with SPI_CS_HOLD.

- **SPI_USR_ADDR_BITLEN**:
  - Value Range: [17, 16, 15, 14, 13]
  - Default Value: 0
  - Description:
    - The bit length in address state.
    - This value is (expected bit number - 1).
    - Can be configured in CONF state. (R/W)

**Section Header:**
Register 30.5. SPI_USER2_REG (0x0018)

**Table Description and Values for Register 30.5:**

- **SPI_USR_COMMAND_VALUE**:
  - Value Range: [31, 27, 26, 25, 24, 23]
  - Default Value: (Reset)
  - Description:
    - The value of command.
    - Can be configured in CONF state. (R/W)

- **SPI_MST_REMPY_ERR_END_EN**:
  - Value Range: [17, 16, 15, 14, 13]
  - Default Value: 0
  - Description:
    - SPI transfer is ended when SPI TX AFIFO read empty error occurs in GP-SPI master full-/half-duplex modes.
    - 0: SPI transfer is not ended when SPI TX AFIFO read empty error occurs in GP-SPI master full-/half-duplex modes. (R/W)

- **SPI_USR_COMMAND_BITLEN**:
  - Value Range: [7, 6, 5, 4, 3]
  - Default Value: 0
  - Description:
    - The bit length of command state.
    - This value is (expected bit number - 1).
    - Can be configured in CONF state. (R/W)

**Footer Information:**
Espressif Systems  
Submit Documentation Feedback

**Document Version and Page Number:**  
ESP32-S3 TRM (Version 1.7)  
Page 1156