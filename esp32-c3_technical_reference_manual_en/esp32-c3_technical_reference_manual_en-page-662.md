

```markdown
Register 27:15. SPI_DIN_NUM_REG (0x0028)

| Bit | Name         | Description                                                                 |
|-----|--------------|-----------------------------------------------------------------------------|
| 31  | (reserved)   |                                                                             |
| 30-8|              |                                                                             |
| 7   | SPI_DIN3_NUM | Configure the delays to input signal FSPIHD based on the setting of SPI_DIN3_MODE. Can be configured in CONF state. (R/W)<br>• 0: delayed by 1 clock cycle<br>• 1: delayed by 2 clock cycles<br>• 2: delayed by 3 clock cycles<br>• 3: delayed by 4 clock cycles |
| 6   | SPI_DIN2_NUM | Configure the delays to input signal FSPIWP based on the setting of SPI_DIN2_MODE. Can be configured in CONF state. (R/W)<br>• 0: delayed by 1 clock cycle<br>• 1: delayed by 2 clock cycles<br>• 2: delayed by 3 clock cycles<br>• 3: delayed by 4 clock cycles |
| 5   | SPI_DIN1_NUM | Configure the delays to input signal FSPIQ based on the setting of SPI_DIN1_MODE. Can be configured in CONF state. (R/W)<br>• 0: delayed by 1 clock cycle<br>• 1: delayed by 2 clock cycles<br>• 2: delayed by 3 clock cycles<br>• 3: delayed by 4 clock cycles |
| 4   | SPI_DINO_NUM | Configure the delays to input signal FSPID based on the setting of SPI_DINO_MODE. Can be configured in CONF state. (R/W)<br>• 0: delayed by 1 clock cycle<br>• 1: delayed by 2 clock cycles<br>• 2: delayed by 3 clock cycles<br>• 3: delayed by 4 clock cycles |
| 3   |              |                                                                             |
| 2   |              |                                                                             |
| 1   |              |                                                                             |
| 0   | Reset        |                                                                             |
```