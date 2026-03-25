

```markdown
Register 11.42. PMU_HP_SLEEP_LP_DIG_POWER_REG (0x00A8)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | PMU_HP_SLEEP_PD_LP_PERI_PD_EN                                              |
| 30  | PMU_HP_SLEEP_LP_MEM_DSLP                                                   |
|     |                                                                             |
| 29  | (reserved)                                                                  |
| ... | ...                                                                         |
| 0   | Reset                                                                       |

PMU_HP_SLEEP_LP_MEM_DSLP Configures whether to enable Memory Deep-sleep mode for the 320 KB SRAM in HP_ACTIVE, HP_MODEM and HP_SLEEP states.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_PD_LP_PERI_PD_EN Configures whether to power down "Peripherals+ROM" domain in HP_ACTIVE, HP_MODEM and HP_SLEEP states.
O: Power up
1: Power down
(R/W)
```