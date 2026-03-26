

```markdown
Register 43.3. SPI_USER_REG (0x0010)

Continued from the previous page...

SPI_RSCK_I_EDGE Configures whether or not to change the polarity of RSCK in slave transfer.
    0: RSCK = !SPI_CK_I
    1: RSCK = SPI_CK_I
    (R/W)

SPI_CK_OUT_EDGE Configures SPI clock mode together with SPI_CK_IDLE_EDGE. Can be configured in CONF state. For more information, see Section 43.7.4.
    (R/W)

SPI_FWRITE_DUAL Configures whether or not to enable the 2-bit mode of read-data phase in write operations.
    0: Not enable
    1: Enable
    Can be configured in CONF state.
    (R/W)

SPI_FWRITE_QUAD Configures whether or not to enable the 4-bit mode of read-data phase in write operations.
    0: Not enable
    1: Enable
    Can be configured in CONF state.
    (R/W)

SPI_FWRITE_OCT Configures whether or not to enable the 8-bit mode of read-data phase in write operations.
    0: Not enable
    1: Enable
    Can be configured in CONF state.
    (R/W)

SPI_USR_CONF_NXT Configures whether or not to enable the CONF state for the next transaction (segment) in a configurable segmented transfer.
    0: This transfer will end after the current transaction (segment) is finished. Or this is not a configurable segmented transfer.
    1: This configurable segmented transfer will continue its next transaction (segment).
    Can be configured in CONF state.
    (R/W)

SPI_SIO Configures whether or not to enable 3-line half-duplex communication, where MOSI and MISO signals share the same pin.
    0: Disable
    1: Enable
    Can be configured in CONF state.
    (R/W)
```