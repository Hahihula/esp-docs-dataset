

```markdown
Register 43.53. SPI_DIN_NUM_REG (0x0028)

| Bit | Name             | Description                                                                 |
|-----|------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)       |                                                                             |
| 30-27|                  |                                                                             |
| 26-24|                  |                                                                             |
| 23-21|                  |                                                                             |
| 20-18|                  |                                                                             |
| 17-15| SPI_DIN3_NUM     | Configures the delays to input signal SPI3_HD based on the setting of SPI_DIN3_MODE. |
| 14-12| SPI_DIN2_NUM     | Configures the delays to input signal SPI3_WP based on the setting of SPI_DIN2_MODE. |
| 11-9 | SPI_DIN1_NUM     | Configures the delays to input signal SPI3_Q based on the setting of SPI_DIN1_MODE. |
| 8   |                  |                                                                             |
| 7   |                  |                                                                             |
| 6   |                  |                                                                             |
| 5   |                  |                                                                             |
| 4   |                  |                                                                             |
| 3   |                  |                                                                             |
| 2   |                  |                                                                             |
| 1   |                  |                                                                             |
| 0   | SPI_DINO_NUM     | Configures the delays to input signal SPI3_D based on the setting of SPI_DINO_MODE. |

SPI_DINO_NUM
Configures the delays to input signal SPI3_D based on the setting of SPI_DINO_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles
(R/W)

SPI_DIN1_NUM
Configures the delays to input signal SPI3_Q based on the setting of SPI_DIN1_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles
(R/W)

SPI_DIN2_NUM
Configures the delays to input signal SPI3_WP based on the setting of SPI_DIN2_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles
(R/W)

SPI_DIN3_NUM
Configures the delays to input signal SPI3_HD based on the setting of SPI_DIN3_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles
(R/W)
```