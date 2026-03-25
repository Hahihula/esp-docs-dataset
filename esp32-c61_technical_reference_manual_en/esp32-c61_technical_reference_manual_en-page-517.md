
```markdown
Register 11.1. PMU_HP_ACTIVE_DIG_POWER_REG (0x0000)

PMU_HP_ACTIVE_VDD_SPI_PD_EN   Configures whether to power down external flash in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_HP_MEM_DSLP    Configures whether to put Internal SRAMx (x= 0, 1, 2) into Deep-sleep mode in HP_ACTIVE state.
O: Do not put Internal SRAM into Deep-sleep
1: Put Internal SRAM into Deep-sleep
(R/W)

PMU_HP_ACTIVE_PD_HP_WIFI_PD_EN   Configures whether to power down MODEM domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_HP_CPU_PD_EN     Configures whether to power down CPU domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_HP_AON_PD_EN      Configures whether to power down Modem Power domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_TOP_PD_EN         Configures whether to power down “Peripherals+ROM” domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)
```