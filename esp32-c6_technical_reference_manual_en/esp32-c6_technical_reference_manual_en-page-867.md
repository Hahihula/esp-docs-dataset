

```markdown
Register 28.3. SPI_USER_REG (0x0010)

Continued from the previous page...

SPI_USR_MOSI_HIGHPART Configures whether or not to enable "high part mode", i.e., only access to high part of the buffers: SPI_W8_REG ~ SPI_W15_REG in write-data phase. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state. (R/W)

SPI_USR_DUMMY_IDLE Configures whether or not to disable SPI clock in DUMMY state. (R/W)
*   0: Not disable
*   1: Disable

Can be configured in CONF state.

SPI_USR_MOSI Configures whether or not to enable the write-data (DOUT) state of an operation. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

SPI_USR_MISO Configures whether or not to enable the read-data (DIN) state of an operation. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

SPI_USR_DUMMY Configures whether or not to enable the DUMMY state of an operation. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

SPI_USR_ADDR Configures whether or not to enable the address (ADDR) state of an operation. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

Continued on the next page...
```