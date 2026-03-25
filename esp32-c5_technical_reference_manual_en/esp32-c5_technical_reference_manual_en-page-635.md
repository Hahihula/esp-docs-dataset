

```markdown
Register 13.21. PMU_HP_SLEEP_DIG_POWER_REG (0x0068)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 23 | 22 | 21 | 20 |
|-----|----|----|----|----|----|----|----|----|----|----|
|     |    |    |    |    |    |    |    |    |    |    |
| Value | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| Reset |    |    |    |    |    |    |    |    |    |    |

PMU_HP_SLEEP_VDD_SPI_PD_EN Configures whether to power down external flash in HP_SLEEP state.
O: Power up
1: Power down
(R/W)

PMU_HP_SLEEP_HP_MEM_DSLP Configures whether to put Internal SRAMx into Deep-sleep mode in HP_SLEEP state.
O: Do not put Internal SRAMx into Deep-sleep
1: Put Internal SRAMx into Deep-sleep
(R/W)

PMU_HP_SLEEP_PD_HP_WIFI_PD_EN Configures whether to power down Modem domain in HP_SLEEP state.
O: Power up
1: Power down
(R/W)

PMU_HP_SLEEP_PD_HP_CPU_PD_EN Configures whether to power down CPU domain in HP_SLEEP state.
O: Power up
1: Power down
(R/W)

PMU_HP_SLEEP_PD_HP_AON_PD_EN Configures whether to power down Modem power domain in HP_SLEEP state.
O: Power up
1: Power down
(R/W)

PMU_HP_SLEEP_PD_TOP_PD_EN Configures whether to power down Peripherals domain in HP_SLEEP state.
O: Power up
1: Power down
(R/W)
```