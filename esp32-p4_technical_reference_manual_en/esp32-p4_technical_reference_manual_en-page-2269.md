

```markdown
Register 43.10. SPI_SLAVE_REG (0x00EO)

| Bit | Name                                      | Description                                                                 |
|-----|-------------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                               |                                                                             |
| 30  | SPI_MST_FD_WAIT_DMA_TX_DATA              |                                                                             |
| 29  | SPI_USR_CONF                             |                                                                             |
| 28  | SPI_SOFT_RESET                           |                                                                             |
| 27  | SPI_SLAVE_MODE                           |                                                                             |
| 26  | (reserved)                               |                                                                             |
| 25  | SPI_DMA_SEG_MAGIC_VALUE                  |                                                                             |
| 24  | (reserved)                               |                                                                             |
| 23  | SPI_SLV_LAST_BYTE_STRB                   |                                                                             |
| 22  | SPI_SLV_WRDMABITLEN                      |                                                                             |
| 21  | SPI_SLV_RDBUF_BITLEN                     |                                                                             |
| 20  | (reserved)                               |                                                                             |
| 19  | SPI_RSCK_DATA_OUT                        |                                                                             |
| 18  | SPI_CLK_MODE_13                          |                                                                             |
| 17  | SPI_CLK_MODE                            |                                                                             |
| 16  | (reserved)                               |                                                                             |
| 15  | O                                       | 0: SPI clock is off when CS becomes inactive.                              |
|     |                                           | 1: SPI clock is delayed one cycle after CS becomes inactive.                |
|     |                                           | 2: SPI clock is delayed two cycles after CS becomes inactive.               |
|     |                                           | 3: SPI clock is always on.                                                  |
|     |                                           | Can be configured in CONF state.                                            |
|     | (R/W)                                    |                                                                             |
| 14  | O                                       | 0: SPI clock mode 1 and mode 3. See Table 43.7-2.                            |
|     |                                           | 1: SPI clock mode 0 and mode 2. See Table 43.7-2.                            |
|     | (R/W)                                    |                                                                             |
| 13  | O                                       | 0: Output data at TSCK rising edge.                                        |
|     |                                           | 1: Output data at RSCK rising edge.                                        |
|     | (R/W)                                    |                                                                             |
| 12  | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 11  | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 10  | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 9   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 8   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 7   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 6   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 5   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 4   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 3   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 2   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 1   | O                                       | 0: Not use                                                                  |
|     |                                           | 1: Use                                                                      |
|     | (R/W)                                    |                                                                             |
| 0   | O                                       | 0: SPI clock is off when CS becomes inactive.                               |
|     |                                           | 1: SPI clock is delayed one cycle after CS becomes inactive.                 |
|     |                                           | 2: SPI clock is delayed two cycles after CS becomes inactive.                |
|     |                                           | 3: SPI clock is always on.                                                  |
|     | (R/W)                                    |                                                                             |

Continued on the next page...
```