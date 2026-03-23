

```markdown
Register 27.3. SPI_USER_REG (0x0010)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     | SPI_USER_COMMAND | SPI_USER_ADDR | SPI_USER_DUMMY | SPI_USER_MISO | SPI_USER_MOSI | SPI_USER_MISO_HIGHPART | SPI_USER_MOSI_HIGHPART | (reserved) | SPI_SIO | SPI_USER_CONF_NXT | SPI_FWRITE_QUAD | (reserved) | SPI_CK_OUT_EDGE | SPI_RSCK_I_EDGE | SPI_CS_HOLD | SPI_CS_SETUP | SPI_TSK_I_EDGE | SPI_QPI_MODE | SPI_DOUTDIN | Reset |
|     | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

SPI_DOUTDIN Set the bit to enable full-duplex communication. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_QPI_MODE 1: Enable QPI mode. 0: Disable QPI mode. This configuration is applicable when the SPI controller works as master or slave. Can be configured in CONF state. (R/W/SS/SC)

SPI_TSK_I_EDGE In slave mode, this bit can be used to change the polarity of TSCK. 0: TSCK = SPI_CK_I. 1: TSCK = !SPI_CK_I. (R/W)

SPI_CS_HOLD Keep SPI CS low when SPI is in DONE state. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_CS_SETUP Enable SPI CS when SPI is in prepare (PREP) state. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_RSCK_I_EDGE In slave mode, this bit can be used to change the polarity of RSCK. 0: RSCK = !SPI_CK_I. 1: RSCK = SPI_CK_I. (R/W)

SPI_CK_OUT_EDGE This bit together with SPI_CK_IDLE_EDGE is used to control SPI clock mode. Can be configured in CONF state. For more information, see Section 27.7.2. (R/W)

SPI_FWRITE_DUAL In write operations, read-data phase is in 2-bit mode. Can be configured in CONF state. (R/W)

SPI_FWRITE_QUAD In write operations, read-data phase is in 4-bit mode. Can be configured in CONF state. (R/W)

SPI_USER_CONF_NXT Enable the CONF state for the next transaction (segment) in a configurable segmented transfer. Can be configured in CONF state. (R/W)
    * If this bit is set, it means this configurable segmented transfer will continue its next transaction (segment).
    * If this bit is cleared, it means this transfer will end after the current transaction (segment) is finished. Or this is not a configurable segmented transfer.

SPI_SIO Set the bit to enable 3-line half-duplex communication, where MOSI and MISO signals share the same pin. 1: enable; 0: disable. Can be configured in CONF state. (R/W)

SPI_USER_MISO_HIGHPART In read-data phase, only access to high-part of the buffers: SPI_W8_REG ~ SPI_W5_REG. 1: enable; 0: disable. Can be configured in CONF state. (R/W)
```