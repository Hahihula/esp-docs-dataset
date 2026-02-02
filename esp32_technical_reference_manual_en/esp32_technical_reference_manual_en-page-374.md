**Chapter Title:**
Chapter 20 SPI Controller (SPI)

**Section Header:**
Register 20.13. SPI_SLV_WR_STATUS_REG (0x30)

**Body Text with Description of Register:**
- **Description:** In the slave mode this register is the status register for the master to write the slave.
- The address length in master mode, if it's bigger than 32 bits,
  - **SPI_ADDR_REG**: stores the higher 32 bits of address value
  - This register also holds rest lower part of an address value. (R/W)

**Register Title:**
Register 20.14. SPI_PIN_REG (0x34)

**Table with Register Bits Description and Values:**

| Bit | Name                          |
|-----|-------------------------------|
| 31-28| Reserved                      |
| 27   | SPI_CS KEEP ACTIVE             |
|     | This bit is only used in master mode where when it is set, the CS signal will keep active. (R/W) |
| 26   | SPI_CK IDLE EDGE               |
|     | This bit is only used in master mode to configure the logic level of SPI output clock in idle state. (R/W) |
|      | - 1: the spi_clk line keeps high when idle; |
|      | - 0: the spi_clk line keeps low when idle. |
| 25   | SPI_MASTER_CK_SEL             |
|     | Reserved                      |
| 24   | SPI_MASTER_CS_POL             |
|     | Reserved                      |
| 23-16| SPI_CK DIS                    |
|      | Reserved                      |
| 15   | SPI_CS2 DIS                   |
|     | This bit enables the SPI CS2 signal. 1: disables CS2; 0: enables CS2. (R/W) |
| 14   | SPI_CS1 DIS                   |
|     | This bit enables the SPI CS1 signal. 1: disables CS1; 0: enables CS1. (R/W) |
| 13-8  | Reserved                      |
|      | - 9, 10, 11, and 12 are reserved for future use or specific functions not detailed in the provided text. |

**Footer Information:** 
Espressif Systems
Page number: 374
Document version: ESP32 TRM (Version 5.6)
Link to Submit Documentation Feedback