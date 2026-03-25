

```markdown
Register 11.1. PMU_HP_ACTIVE_DIG_POWER_REG (0x0000)

| Bit | 31 | 30 | 29 | 28 | 27 | 26 | 23 | 22 | 21 | 20 | ... | Reset |
|-----|----|----|----|----|----|----|----|----|----|----|------|-------|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | ...  | 0     |

PMU_HP_ACTIVE_VDD_SPI_PD_EN Configures whether to power down external flash in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_HP_MEM_DSLP Configures whether to put Internal SRAMx into Deep-sleep mode in HP_ACTIVE state.
O: Do not put Internal SRAMx into Deep-sleep
1: Put Internal SRAMx into Deep-sleep
(R/W)

PMU_HP_ACTIVE_PD_HP_MODEM_PD_EN Configures whether to power down Modem power domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_HP_CPU_PD_EN Configures whether to power down CPU power domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)

PMU_HP_ACTIVE_PD_TOP_PD_EN Configures whether to power down Peripherals power domain in HP_ACTIVE state.
O: Power up
1: Power down
(R/W)
```