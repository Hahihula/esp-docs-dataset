

```markdown
Chapter 27 SPI Controller (SPI)
Register 27.3. SPI_USER_REG (0x0010)

Continued from the previous page...

SPI_USR_MOSI_HIGHPART In write-data phase, only access to high-part of the buffers:  
SPI_W8_REG ~ SPI_W15_REG. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_USR_DUMMY_IDLE If this bit is set, SPI clock is disabled in DUMMY state. Can be configured in CONF state. (R/W)

SPI_USER_MOSI Set this bit to enable the write-data (DOUT) state of an operation. Can be configured in CONF state. (R/W)

SPI_USR_MISO Set this bit to enable the read-data (DIN) state of an operation. Can be configured in CONF state. (R/W)

SPI_USR_DUMMY Set this bit to enable the DUMMY state of an operation. Can be configured in CONF state. (R/W)

SPI_USR_ADDR Set this bit to enable the address (ADDR) state of an operation. Can be configured in CONF state. (R/W)

SPI_USR_COMMAND Set this bit to enable the command (CMD) state of an operation. Can be configured in CONF state. (R/W)
```