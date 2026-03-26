

```markdown
Register 43.79. LP_SPI_USER_REG (0x0010)

Continued from the previous page...

LP_SPI_USR_MISO_HIGHPART Configures whether or not to enable High-Part mode in read-data phase, i.e., only access to high-part of the buffers: LP_SPI_W8_REG ~ LP_SPI_W15_REG.
O: Disable
1: Enable
(R/W)

LP_SPI_USR_MOSI_HIGHPART Configures whether or not to enable High-Part mode in write-data phase, i.e., only access to high-part of the buffers: LP_SPI_W8_REG ~ LP_SPI_W15_REG.
O: Disable
1: Enable
(R/W)

LP_SPI_USR_DUMMY_IDLE Configures whether or not to disable SPI clock in DUMMY state.
O: Not disable
1: Disable
(R/W)

LP_SPI_USR_MOSI Configures whether or not to enable the write-data (DOUT) state of an operation.
O: Disable
1: Enable
(R/W)

LP_SPI_USR_MISO Configures whether or not to enable the read-data (DIN) state of an operation.
O: Disable
1: Enable
(R/W)

LP_SPI_USR_DUMMY Configures whether or not to enable the DUMMY state of an operation.
O: Disable
1: Enable
(R/W)

LP_SPI_USR_ADDR Configures whether or not to enable the address (ADDR) state of an operation.
O: Disable
1: Enable
(R/W)

LP_SPI_USR_COMMAND Configures whether or not to enable the command (CMD) state of an operation.
O: Disable
1: Enable
(R/W)
```