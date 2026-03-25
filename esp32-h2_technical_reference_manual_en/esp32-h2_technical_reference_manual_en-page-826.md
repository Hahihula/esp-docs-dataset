

```markdown
Register 29.15. SPI_DIN_NUM_REG (0x0028)

| Bit | Name         | Description                                                                 |
|-----|--------------|-----------------------------------------------------------------------------|
| 31  |              | (reserved)                                                                  |
| 30  |              | (reserved)                                                                  |
| 29  |              | (reserved)                                                                  |
| 28  |              | (reserved)                                                                  |
| 27  |              | (reserved)                                                                  |
| 26  |              | (reserved)                                                                  |
| 25  |              | (reserved)                                                                  |
| 24  |              | (reserved)                                                                  |
| 23  |              | (reserved)                                                                  |
| 22  |              | (reserved)                                                                  |
| 21  |              | (reserved)                                                                  |
| 20  |              | (reserved)                                                                  |
| 19  |              | (reserved)                                                                  |
| 18  |              | (reserved)                                                                  |
| 17  |              | (reserved)                                                                  |
| 16  |              | (reserved)                                                                  |
| 15  |              | (reserved)                                                                  |
| 14  |              | (reserved)                                                                  |
| 13  |              | (reserved)                                                                  |
| 12  |              | (reserved)                                                                  |
| 11  |              | (reserved)                                                                  |
| 10  |              | (reserved)                                                                  |
| 9   |              | (reserved)                                                                  |
| 8   |              | (reserved)                                                                  |
| 7   |              | (reserved)                                                                  |
| 6   |              | (reserved)                                                                  |
| 5   |              | (reserved)                                                                  |
| 4   |              | (reserved)                                                                  |
| 3   |              | (reserved)                                                                  |
| 2   |              | (reserved)                                                                  |
| 1   |              | (reserved)                                                                  |
| 0   | Reset        |                                                                             |

SPI_DINO_NUM Configures the delays to input signal FSPID based on the setting of SPI_DINO_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state. (R/W)

SPI_DIN1_NUM Configures the delays to input signal FSPIQ based on the setting of SPI_DIN1_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state. (R/W)

SPI_DIN2_NUM Configures the delays to input signal FSPIWP based on the setting of SPI_DIN2_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state. (R/W)

SPI_DIN3_NUM Configures the delays to input signal FSPIHD based on the setting of SPI_DIN3_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state. (R/W)
```