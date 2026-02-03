**Chapter Title:**
Chapter 30 SPI Controller (SPI)

**Register Information:**

- **Register Name:** Register 30.1. SPI_CMD_REG (0x0000)
  
  - **Field Description:**
    - `SPI_CONF_BITLEN`:
      - **Description:** Define the cycles of APB_CLK in CONF state.
      - **Access Mode:** Can be configured in CONF state. (R/W)

- **Register Name:** SPI_UPDATE
  - Set this bit to synchronize SPI registers from APB clock domain into SPI module clock domain. This bit is only used in SPI master mode. (WT)
  
- **Register Name:** SPI_USR
  - User-defined command enable.
  - An SPI operation will be triggered when the bit is set.
  - The bit will be cleared once the operation is done: 
    - `1`: enable
    - `0`: disable
  - Can not be changed by CONF_buf. (R/W/SC)

- **Register Name:** Register 30.2. SPI_ADDR_REG (0x0004)
  
  - **Field Description:**
    - `SPI_USR_ADDR_VALUE`
      - Address to slave.
      - Can be configured in CONF state. (R/W)

**Footer Information:**
- Page Number: 1153
- Document Title: ESP32-S3 TRM (Version 1.7)
- Company Name: Espressif Systems

**Navigation Links:** 
- GoBack