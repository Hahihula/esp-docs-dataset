

```markdown
Register 13.31. PMU_HP_SLEEP_LP_REGULATORO_REG (0x009C)

| 31 | 27 | 26 | 23 | 22 | 21 | 20 |
|----:|----:|----:|----:|----:|----:|----:|
|    |     |     |     | PMU_HP_SLEEP_LP_REGULATOR_XPD | (reserved) |         |
|    |     |     |     |                             |           |         |

PMU_HP_SLEEP_LP_REGULATOR_XPD Configures whether to enable the LP sys regulator in HP_SLEEP state.
O: Disable the LP sys regulator
1: Enable the LP sys regulator
(R/W)

Register 13.32. PMU_HP_SLEEP_LP_DIG_POWER_REG (0x00A8)

| 31 | 30 | 29 |
|----:|----:|----:|
|    |     | PMU_HP_SLEEP_PD_LP_PERI_PD_EN | PMU_HP_SLEEP_LP_MEM_DSLP | (reserved) |

PMU_HP_SLEEP_LP_MEM_DSLP Configures whether to enable Memory Deep-sleep mode for the 16 KB SRAM in HP_ACTIVE/HP_MODEM/HP_SLEEP state.
O: Disable
1: Enable
(R/W)

PMU_HP_SLEEP_PD_LP_PERI_PD_EN Configures whether to power down LP PD Peripherals domain in HP_ACTIVE/HP_MODEM/HP_SLEEP state.
O: Power up
1: Power down
(R/W)
```