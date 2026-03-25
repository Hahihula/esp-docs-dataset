

```markdown
Register 11.67. PMU_POWER_HP_PAD_REG (0x0118)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 2   | 1                             | Reset                                                                       |
| 1   | PMU_FORCE_HP_PAD_ISO_ALL      | Configures whether or not to enable HP GPIOs to enable ISO signal. This setting has a lower priority than PMU_FORCE_HP_PAD_ISO_ALL.<br>0: No effect<br>1: Disable (R/W) |
| 0   | PMU_FORCE_HP_PAD_NO_ISO_ALL   | Configures whether or not to disable HP GPIOs to enable ISO signal. This setting has a higher priority than PMU_FORCE_HP_PAD_NO_ISO_ALL.<br>0: No effect<br>1: Enable (R/W) |

Register 11.68. PMU_POWER_VDD_SPI_CNTL_REG (0x011C)

| Bit | Field Name                     | Description                                                                 |
|-----|--------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 3   | 0                             | Reset                                                                       |
| 2   | Oxff                          |                                                                             |
| 18  | PMU_VDD_SPI_PWR_WAIT          | Configures the number of cycles to delay before powering up or down the VDD_SPI cell. (R/W) |
| 17  | PMU_VDD_SPI_PWR_SW            | Configure the power switch signal of VDD_SPI cell of HP GPIOs. (R/W)         |
| 16  | PMU_VDD_SPI_PWR_SEL_SW        | Configure to select the power switch control signals of VDD_SPI cell of HP GPIOs.<br>0: controlled by PMU<br>1: controlled by PMU_VDD_SPI_PWR_SW (R/W) |
```