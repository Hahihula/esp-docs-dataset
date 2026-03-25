

```markdown
Chapter 11 Low-Power Management  
GoBack

Register 11.19. PMU_HP_SLEEP_HP_REGULATOREO_REG (0x0090)

| 31 | ... | 19 | 18 | 17 | ... | 0 |
|----|-----|----|----|----|-----|---|
|   |     |    | O  | 1  | 0   | Reset |

PMU_HP_SLEEP_HP_REGULATOR_XPD Configures whether to enable the HP sys regulator in HP_SLEEP state.  
O: Disable  
1: Enable  
(R/W)

Register 11.20. PMU_HP_SLEEP_XTAL_REG (0x0098)

| 31 | 30 | ... | 0 |
|----|----|-----|---|
| 1  | O  | ... | Reset |

PMU_HP_SLEEP_XPD_XTAL Configures whether to enable XTAL_CLK analog source in HP_SLEEP state.  
O: Disable  
1: Enable  
(R/W)
```