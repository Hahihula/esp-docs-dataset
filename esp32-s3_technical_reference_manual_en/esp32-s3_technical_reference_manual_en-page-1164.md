**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**GoBack Link:** GoBack

---

### Register Section:

#### Register Name and Address:
- **Register 30.12, SPI_SLAVE_REG (0x00E4)**

##### Registers Description with Values in Hexadecimal Format:
- **SPI_SLV_LAST_ADDR**
  - Bits: [31, 26, 25, 18, 17, 0]
  - Values: [O, O, O, Reset]

- **SPI_SLV_DATA_BITLEN**
  - Description: Configure the transferred data bit length in SPI slave full-/half-duplex modes. (R/W/SS)

- **SPI_SLV_LAST_COMMAND**
  - In Slave mode, it is the value of command. (R/W/SS)
  
- **SPI_SLVLast_ADDR**
  - In Slave mode, it is the value of address. (R/W/SS)

---

#### Register Name and Address:
- **Register 30.13, SPI_CLOCK_REG (0x000C)**

##### Registers Description with Values in Hexadecimal Format:

- **SPI_CLK_EQU_SYSCLK**
  - Bits: [31, 26, 25, 18, 17, 11, 10, 9, 6, 5, 4]
  - Values: [Reset, O, Ox3, Ox1]

- **SPI_CLKCNT_L**
  - In master mode, this field must be equal to SPI_CLKCNT_N. In slave mode, it must be 0. Can be configured in CONF state.

- **SPI_CLKCNT_H**
  - In master mode, this field must be floor((SPI_CLKCNT_N + 1)/2 - 1). floor() here is to down round a number, floor(2.2) = 2. In slave mode, it must be 0. Can be configured in CONF state.

- **SPI_CLKCNT_N**
  - In master mode, this is the divider of SPI_CLK. So SPI_CLK frequency is f_apb_clk / (SPI_CLKDIV_P + 1)/ (SPI_CLKCNT_N + 1). Can be configured in CONF state.
  
- **SPI_CLKDIV_PRE**
  - In master mode, this is pre-divider of SPI_CLK. Can be configured in CONF state.

- **SPI_CLK_EQU_SYSCLK**
  - In master mode: 1; SPI_CLK is equal to APB_CLK. 0: SPI_CLK is divided from APB_CLK. Can be configured in CONF state.
  
---

**Footer Information:** 
Espressif Systems
ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback

**Page Number and Document Version:** Page number not visible, but document version mentioned as "Version 1.7"