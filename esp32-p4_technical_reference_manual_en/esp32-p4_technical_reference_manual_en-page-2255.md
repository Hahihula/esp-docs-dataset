

```markdown
Register 43.3. SPI_USER_REG (0x0010)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | (reserved) | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|----|----|------------|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|---|---|
| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | (reserved) | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | Reset |

SPI_DOUTDIN Configures whether or not to enable full-duplex communication.
O: Disable
1: Enable
Can be configured in CONF state.
(R/W)

SPI_QPI_MODE Configures whether or not to enable QPI mode.
O: Disable
1: Enable
This configuration is applicable when the SPI controller works as master or slave. Can be configured in CONF state.
(R/W/SS/SC)

SPI_OPI_MODE Configures whether or not to enable OPI mode.
O: Disable. SPI controller works in other modes.
1: Enable. SPI controller works in OPI mode, all phases of which are in 8-bit mode.
This configuration is only applicable when the SPI controller works as master. Can be configured in CONF state.
(R/W)

SPI_TSCK_I_EDGE Configures whether or not to change the polarity of TSCK in slave transfer.
O: TSCK = SPI_CK_I
1: TSCK = !SPI_CK_I
(R/W)

SPI_CS_HOLD Configures whether or not to keep SPI CS low when SPI is in DONE state.
O: Not keep low
1: Keep low
Can be configured in CONF state.
(R/W)

SPI_CS_SETUP Configures whether or not to enable SPI CS when SPI is in prepare (PREP) state.
O: Disable
1: Enable
Can be configured in CONF state.
(R/W)
```