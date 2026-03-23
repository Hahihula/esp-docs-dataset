

```markdown
Register 28.3. SPI_USER_REG (0x0010)

Continued from the previous page...

SPI_USR_COMMAND Configures whether or not to enable the command (CMD) state of an operation. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

Register 28.4. SPI_USER1_REG (0x0014)

| Bit | Description                  |
|-----|------------------------------|
| 31  | SPI_USR_ADDR_BITLEN          |
| 27  |                              |
| 26  |                              |
| 22  | SPI_CS_HOLD_TIME             |
| 21  |                              |
| 17  | SPI_CS_SETUP_TIME            |
| 16  | SPI_MST_WFULL_ERR_END_EN     |
| (reserved) |                      |
| 8   | SPI_USR_DUMMY_CYCLELEN       |
| 7   |                              |
| 0   | Reset                        |

SPI_USR_DUMMY_CYCLELEN Configures the length of DUMMY state. (R/W)
Measurement unit: SPI_CLK clock cycles.
This value is (the expected cycle number - 1). Can be configured in CONF state.

SPI_MST_WFULL_ERR_END_EN Configures whether or not to end the SPI transfer when SPI RX AFIFO wfull error occurs in master full-/half-duplex transfers. (R/W)
*   0: Not end
*   1: End

SPI_CS_SETUP_TIME Configures the length of prepare (PREP) state. (R/W)
Measurement unit: SPI_CLK clock cycles.
This value is equal to the expected cycles - 1. This field is used together with SPI_CS_SETUP.
Can be configured in CONF state.

SPI_CS_HOLD_TIME Configures the delay cycles of CS pin. (R/W)
Measurement unit: SPI_CLK clock cycles.
This field is used together with SPI_CS_HOLD. Can be configured in CONF state.

SPI_USR_ADDR_BITLEN Configures the bit length in address state. (R/W)
This value is (expected bit number - 1). Can be configured in CONF state.
```