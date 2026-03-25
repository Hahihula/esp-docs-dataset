

```markdown
Register 29.3. SPI_USER_REG (0x0010)

Continued from the previous page...

SPI_FWRITE_QUAD Configures whether or not to enable the 4-bit mode of read-data phase in write operations.
O: Not enable
1: Enable
Can be configured in CONF state. (R/W)

SPI_USR_CONF_NXT Configures whether or not to enable the CONF state for the next transaction (segment) in a configurable segmented transfer.
O: this transfer will end after the current transaction (segment) is finished. Or this is not a configurable segmented transfer.
1: this configurable segmented transfer will continue its next transaction (segment).
Can be configured in CONF state. (R/W)

SPI_SIO Configures whether or not to enable 3-line half-duplex communication, where MOSI and MISO signals share the same pin.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_USR_MISO_HIGHPART Configures whether or not to enable "high part mode", i.e., only access to high part of the buffers: SPI_W8_REG ~ SPI_W15_REG in read-data phase.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_USR_MOSI_HIGHPART Configures whether or not to enable "high part mode", i.e., only access to high part of the buffers: SPI_W8_REG ~ SPI_W15_REG in write-data phase.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_USR_DUMMY_IDLE Configures whether or not to disable SPI clock in DUMMY state.
O: Not disable
1: Disable
Can be configured in CONF state. (R/W)

SPI_USR_MOSI Configures whether or not to enable the write-data (DOUT) state of an operation.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)

SPI_USR_MISO Configures whether or not to enable the read-data (DIN) state of an operation.
O: Disable
1: Enable
Can be configured in CONF state. (R/W)
```