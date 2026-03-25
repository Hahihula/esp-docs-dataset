
```markdown
Register 11.66. PMU_POWER_PD_MEM_MASK_REG (0x0114)

| 31 | 27 | 26 | 22 | 21 | 17 | 16 | 15 | 14 | 10 | 9 | 5 | 4 | 0 |
|----|----|----|----|----|----|----|----|----|----|---|---|---|---|
|    | 0  | 0  | 0  | 0  | 0  | 0  | 0  | O  | 0  | 0 | 0 | 0 | Reset |

PMU_PD_HP_MEM2_PD_MASK Configures whether the Internal SRAM2 follows the power up/down state of "Peripherals+ROM" domain.
O: Follows "Peripherals+ROM" domain
1: Does not follow "Peripherals+ROM" domain.
(R/W)

PMU_PD_HP_MEM1_PD_MASK Configures whether the Internal SRAM1 follows the power up/down state of "Peripherals+ROM" domain.
O: Follows "Peripherals+ROM" domain
1: Does not follow "Peripherals+ROM" domain.
(R/W)

PMU_PD_HP_MEM0_PD_MASK Configures whether the Internal SRAM0 follows the power up/down state of "Peripherals+ROM" domain.
O: Follows "Peripherals+ROM" domain
1: Does not follow "Peripherals+ROM" domain.
(R/W)

PMU_PD_HP_MEM2_MASK Configures whether to force power up Internal SRAM2.
O: Do not force power up
1: Force power up
(R/W)

PMU_PD_HP_MEM1_MASK Configures whether to to force power up Internal SRAM1.
O: Do not force power up
1: Force power up
(R/W)

PMU_PD_HP_MEM0_MASK Configures whether to force power up Internal SRAM0.
O: Do not force power up
1: Force power up
(R/W)
```