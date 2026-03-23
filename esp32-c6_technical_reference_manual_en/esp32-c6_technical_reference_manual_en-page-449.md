

```markdown
Register 12.11. PMU_HP_MODEM_DIG_POWER_REG (0x0034)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | Reserved                             |                                                                             |
| 30  | PMU_HP_MODEM_PD_TOP_PD_EN            | Configures whether to power down Peripherals domain in HP_MODEM state.       |
| 29  | PMU_HP_MODEM_PD_HP_AON_PD_EN         | Configures whether to power down Modem power domain in HP_MODEM state.      |
| 28  | PMU_HP_MODEM_PD_HP_CPU_PD_EN         | Configures whether to power down CPU domain in HP_MODEM state.              |
| 27  | PMU_HP_MODEM_PD_WIFI_PD_EN          | Configures whether to power down Modem domain in HP_MODEM state.            |
| 26  | (reserved)                           |                                                                             |
| 25  | PMU_HP_MODEM_VDD_SPI_PD_EN           | Configures whether to power down external flash in HP_MODEM state.          |
| 24  | PMU_HP_MODEM_HP_MEM_DSLP             | Configures whether to put Internal SRAMx into Deep-sleep mode in HP_MODEM state. |
| 23  | (reserved)                           |                                                                             |
| 22  | PMU_HP_MODEM_PD_HP_AON_PD_EN         | Configures whether to power down Modem power domain in HP_MODEM state.      |
| 21  | PMU_HP_MODEM_VDD_SPI_PD_EN           | Configures whether to power down external flash in HP_MODEM state.          |
| 20  | (reserved)                           |                                                                             |

PMU_HP_MODEM_VDD_SPI_PD_EN   Configures whether to power down external flash in
HP_MODEM state.
O: Power up
1: Power down
(R/W)

PMU_HP_MODEM_HP_MEM_DSLP     Configures whether to put Internal SRAMx into Deep-sleep
mode in HP_MODEM state.
O: Do not put Internal SRAMx into Deep-sleep
1: Put Internal SRAMx into Deep-sleep
(R/W)

PMU_HP_MODEM_PD_HP_WIFI_PD_EN Configures whether to power down Modem domain in
HP_MODEM state.
O: Power up
1: Power down
(R/W)

PMU_HP_MODEM_PD_HP_CPU_PD_EN Configures whether to power down CPU domain in
HP_MODEM state.
O: Power up
1: Power down
(R/W)

PMU_HP_MODEM_PD_HP_AON_PD_EN Configures whether to power down Modem power domain in
HP_MODEM state.
O: Power up
1: Power down
(R/W)

PMU_HP_MODEM_PD_TOP_PD_EN    Configures whether to power down Peripherals domain in
HP_MODEM state.
O: Power up
1: Power down
(R/W)
```