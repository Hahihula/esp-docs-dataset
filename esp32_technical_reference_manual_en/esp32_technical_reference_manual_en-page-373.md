**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Register Information and Descriptions:**

1. **Register Name:** Register 20.10, SPI_USER2_REG (0x24)
   - **Field Description:**
     - **SPI_USR_COMMAND_BITLEN**: Indicates the bit length of the command phase minus one in SPI half-duplex mode and QSPI mode.
       - It is only valid when SPI_USR_COMMAND is set to 1. (Read/Write)

     - **SPI_USR_COMMAND_VALUE**: Indicates the value of the command to be transmitted in SPI half-duplex mode and QSPI mode.
       - It is only valid when SPI_USR_COMMAND is set to 1. (Read/Write)

2. **Register Name:** Register 20.11, SPI_MOSI_DLEN_REG (0x28)
   - **Field Description:**
     - **SPI_USR_MOSI_DBITLEN**: Indicates the length of MOSI data minus one, in multiples of one bit.
       - It is only valid when SPI_USR_MOSI is set to 1 in master mode. (Read/Write)

3. **Register Name:** Register 20.12, SPI_MISO_DLEN_REG (0x2C)
   - **Field Description:**
     - **SPI_USR_MISO_DBITLEN**: Indicates the length of MISO data minus one, in multiples of one bit.
       - It is only valid when SPI_USR_MISO is set to 1 in master mode. (Read/Write)

**Footer Information:** 
- Page number and document version: "373 ESP32 TRM (Version 5.6)"
- Company name: Espressif Systems
- Link for submitting documentation feedback

**Navigation Links:**
- GoBack button at the top right corner of each section.

**Visual Elements Description:**

Each register description is accompanied by a visual representation showing bit positions and their corresponding values, with reserved bits marked as (reserved). The registers are labeled clearly to indicate which specific fields within them correspond to different functions.