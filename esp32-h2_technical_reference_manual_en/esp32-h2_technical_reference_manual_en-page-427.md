

```markdown
Register 11.26. PMU_POWER_PD_MEM_MASK_REG (0x0110)

| Bit Range | Field Name                     |
|-----------|--------------------------------|
| 31        | (reserved)                    |
| 27-26     | PMU_PD_HP_MEM1_MASK           |
| 22-21     | PMU_PD_HP_MEM2_MASK           |
| 17-15     | (reserved)                    |
| 9         | PMU_PD_HP_MEM1_PD_MASK        |
| 5-4       | PMU_PD_HP_MEM2_PD_MASK        |
| 0         | Reset                         |

PMU_PD_HP_MEM2_PD_MASK Configures whether the Internal SRAM2 domain follows the power up/down state of the Peripherals domain.
0: Follows Peripherals domain
1: Does not follow Peripherals domain.
(R/W)

PMU_PD_HP_MEM1_PD_MASK Configures whether the Internal SRAM1 domain follows the power up/down state of the Peripherals domain.
0: Follows Peripherals domain
1: Does not follow Peripherals domain.
(R/W)

PMU_PD_HP_MEM2_MASK Configures whether to force power up Internal SRAM2.
0: Do not force power up
1: Force power up
(R/W)

PMU_PD_HP_MEM1_MASK Configures whether to to force power up Internal SRAM1.
0: Do not force power up
1: Force power up
(R/W)
```

```markdown
Register 11.27. PMU_POWER_CK_WAIT_CNTL_REG (0x011C)

| Bit Range | Field Name                     |
|-----------|--------------------------------|
| 31        | (PMU_WAIT_PLL_STABLE)          |
|           |                                |
|           | (PMU_WAIT_XTAL_STABLE)         |
|           |                                |
| 16-15     | 0x0100                         |
| 0         | Reset                          |

PMU_WAIT_PLL_STABLE Configures the number of CLK_DYN_FAST_CLK cycles after which PLL_CLK gate opening is enabled. (R/W)

PMU_WAIT_XTAL_STABLE Configures the number of CLK_DYN_FAST_CLK cycles after which XTAL_CLK gate opening is enabled. (R/W)
```