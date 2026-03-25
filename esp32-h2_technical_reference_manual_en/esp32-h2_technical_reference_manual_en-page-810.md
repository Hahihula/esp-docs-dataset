

```markdown
Register 29.3. SPI_USER_REG (0x0010)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|
|     | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 0  | 0  | 0  | 0  | 0  | Reset |

SPI_DOUTDIN Configures whether or not to enable full-duplex communication.
- 0: Disable
- 1: Enable
Can be configured in CONF state. (R/W)

SPI_QPI_MODE Configures whether or not to enable QPI mode.
- 0: Disable
- 1: Enable
This configuration is applicable when the SPI controller works as master or slave. Can be configured in CONF state. (R/W/SS/SC)

SPI_TSCK_I_EDGE Configures whether or not to change the polarity of TSCK in slave transfer.
- 0: TSCK = SPI_CK_I
- 1: TSCK = !SPI_CK_I
(R/W)

SPI_CS_HOLD Configures whether or not to keep SPI CS low when SPI is in DONE state.
- 0: Not keep low
- 1: Keep low
Can be configured in CONF state. (R/W)

SPI_CS_SETUP Configures whether or not to enable SPI CS when SPI is in prepare (PREP) state.
- 0: Disable
- 1: Enable
Can be configured in CONF state. (R/W)

SPI_RSCK_I_EDGE Configures whether or not to change the polarity of RSCK in slave transfer.
- 0: RSCK = !SPI_CK_I
- 1: RSCK = SPI_CK_I
(R/W)

SPI_CK_OUT_EDGE Configures SPI clock mode together with SPI_CK_IDLE_EDGE.
Can be configured in CONF state. For more information, see Section 29.7.2. (R/W)

SPI_FWRITE_DUAL Configures whether or not to enable the 2-bit mode of read-data phase in write operations.
- 0: Not enable
- 1: Enable
Can be configured in CONF state. (R/W)
```

Continued on the next page...
```