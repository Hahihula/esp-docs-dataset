

```markdown
Chapter 43 SPI Controller (SPI) GoBack


Register 43.86. LP_SPI_SLEEP_CONFO_REG (0x0044)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | LP_SPI_SLEEP_WK_DATA_SEL                                                   |
| 29  | LP_SPI_SLEEP_DIS_RXFIFO_WR_EN                                              |
| 28  | LP_SPI_SLEEP_RXFIFO_WR_EN                                                  |
| 27  | LP_SPI_SLV_WK_MODE_SEL                                                     |
| 26  | LP_SPI_SLV_WK_CHAR_MASK                                                    |
| 25  | LP_SPI_SLV_WK_CHAR_NUM                                                      |
| 24  | LP_SPI_SLV_WK_CHAR0                                                         |
|     | Reset                                                                       |

LP_SPI_SLV_WK_CHAR0 (R/W) Configures wake-up character 0.

LP_SPI_SLV_WK_CHAR_NUM (R/W) Configures the amount of the enabled wake-up characters.

LP_SPI_SLV_WK_CHAR_MASK (R/W) Configures the bit map for the characters to be masked.
Bit 0 ~ bit 4 correspond to wake-up character 0 ~ character 4, respectively.
If the bit value is:
- 0: The corresponding wake-up character is not masked.
- 1: The corresponding wake-up character is masked.

LP_SPI_SLV_WK_MODE_SEL (R/W) Configures the wake-up mode.
0: Wakes up the chip once the LP-SPI slave detects a start bit.
1: Wakes up the chip once the LP-SPI slave detects a specific sequence of characters.

LP_SPI_SLEEP_EN (R/W) Configures whether or not to enable sleep mode.
0: Not enable
1: Enable

LP_SPI_SLEEP_DIS_RXFIFO_WR_EN (R/W) Configures whether or not to store the data before wake-up.
0: Store the data
1: Not store the data

LP_SPI_SLEEP_WK_DATA_SEL (R/W) Configures in which states to detect the wake-up characters.
0: Only detect wake-up characters from RX data in DATA state.
1: Detect wake-up characters from RX data in all states.
```