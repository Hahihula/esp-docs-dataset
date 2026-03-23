

```markdown
Register 28.3. SPI_USER_REG (0x0010)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 0 | 0 | 0 | 0 | Reset |

SPI_DOUTDIN Configures whether or not to enable full-duplex communication. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

SPI_QPI_MODE Configures whether or not to enable QPI mode. (R/W/SS/SC)
*   0: Disable
*   1: Enable

This configuration is applicable when the SPI controller works as master or slave. Can be configured in CONF state.

SPI_TSCK_I_EDGE Configures whether or not to change the polarity of TSCK in slave transfer. (R/W)
*   0: TSCK = SPI_CK_I
*   1: TSCK = !SPI_CK_I

SPI_CS_HOLD Configures whether or not to keep SPI CS low when SPI is in DONE state. (R/W)
*   0: Not keep low
*   1: Keep low

Can be configured in CONF state.

SPI_CS_SETUP Configures whether or not to enable SPI CS when SPI is in prepare (PREP) state. (R/W)
*   0: Disable
*   1: Enable

Can be configured in CONF state.

SPI_RSCK_I_EDGE Configures whether or not to change the polarity of RSCK in slave transfer. (R/W)
*   0: RSCK = !SPI_CK_I
*   1: RSCK = SPI_CK_I

Continued on the next page...
```