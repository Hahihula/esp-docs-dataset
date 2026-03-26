

```markdown
Register 43.79. LP_SPI_USER_REG (0x0010)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | (reserved) | LP_SPI_SIO | (reserved) | LP_SPI_DOUTDIN |
|     |    |    | LP_SPI_USER_COMMAND | LP_SPI_USER_ADDR | LP_SPI_USER_MISO | LP_SPI_USER_MOSI | LP_SPI_USER_IDLE | LP_SPI_HIGHPART | LP_SPI_LOWPART | LP_SPI_SCK_OUT_EDGE | LP_SPI_RSCK_I_EDGE | LP_SPI_CS_HOLD | LP_SPI_CS_SETUP | LP_SPI_TSCK_I_EDGE |
```

LP_SPI_DOUTDIN Configures whether or not to enable full-duplex communication.
0: Disable
1: Enable
(R/W)

LP_SPI_TSCK_I_EDGE Configures whether or not to change the polarity of TSCK in slave transfer.
0: TSCK = SPI_CK_I
1: TSCK = !SPI_CK_I
(R/W)

LP_SPI_CS_HOLD Configures whether or not to keep SPI CS low when SPI is in DONE state.
0: Not keep low
1: Keep low
(R/W)

LP_SPI_CS_SETUP Configures whether or not to enable SPI CS when SPI is in prepare (PREP) state.
0: Disable
1: Enable
(R/W)

LP_SPI_RSCK_I_EDGE Configures whether or not to change the polarity of RSCK in slave transfer.
0: RSCK = !SPI_CK_I
1: RSCK = SPI_CK_I
(R/W)

LP_SPI_CK_OUT_EDGE Configures SPI clock mode together with LP_SPI_CK_IDLE_EDGE.
For more information, see Section 43.7.4. (R/W)

LP_SPI_SIO Configures whether or not to enable 3-line half-duplex communication, where MOSI and MISO signals share the same pin.
0: Disable
1: Enable
(R/W)
```