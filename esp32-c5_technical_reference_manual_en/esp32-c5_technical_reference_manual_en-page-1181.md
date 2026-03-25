

```markdown
Register 33.15. SPI_DIN_NUM_REG (0x0028)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    | SPI_DIN7_NUM | SPI_DIN6_NUM | SPI_DIN5_NUM | SPI_DIN4_NUM | SPI_DIN3_NUM | SPI_DIN2_NUM | SPI_DIN1_NUM | SPI_DINO_NUM |
| 0   | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

SPI_DINO_NUM Configures the delays to input signal FSPID based on the setting of SPI_DINO_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state.
(R/W)

SPI_DIN1_NUM Configures the delays to input signal FSPIQ based on the setting of SPI_DIN1_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state.
(R/W)

SPI_DIN2_NUM Configures the delays to input signal FSPIWP based on the setting of SPI_DIN2_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state.
(R/W)

SPI_DIN3_NUM Configures the delays to input signal FSPIHD based on the setting of SPI_DIN3_MODE.
- 0: Delayed by 1 clock cycle
- 1: Delayed by 2 clock cycles
- 2: Delayed by 3 clock cycles
- 3: Delayed by 4 clock cycles

Can be configured in CONF state.
(R/W)

SPI_DIN4_NUM Reserved (HRO)
SPI_DIN5_NUM Reserved (HRO)
SPI_DIN6_NUM Reserved (HRO)
SPI_DIN7_NUM Reserved (HRO)
```