

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| PMU_HP_MODEM_SYSCLK_REG                   | System clock control register in HP_MODEM state                                                | 0x0058  | R/W    |
| PMU_HP_MODEM_HP_REGULATORO_REG            | HP sys regulator power control register in HP_MODEM state                                      | 0x005C  | R/W    |
| PMU_HP_MODEM_XTAL_REG                     | XTAL_CLK power control register in HP_MODEM state                                              | 0x0064  | R/W    |
| PMU_HP_SLEEP_DIG_POWER_REG                | Digital power domain control register in HP_SLEEP state                                        | 0x0068  | R/W    |
| PMU_HP_SLEEP_ICG_HP_FUNC_REG              | HP system peripheral’s function clock control register in HP_SLEEP state                      | 0x006C  | R/W    |
| PMU_HP_SLEEP_ICG_HP_APB_REG               | HP system peripheral’s APB clock control register in HP_SLEEP state                           | 0x0070  | R/W    |
| PMU_HP_SLEEP_HP_SYS_CNTL_REG              | System control register in HP_SLEEP state                                                     | 0x0078  | R/W    |
| PMU_HP_SLEEP_HP_CK_POWER_REG              | Clock source power control register in HP_SLEEP state                                         | 0x007C  | R/W    |
| PMU_HP_SLEEP_BACKUP_REG                   | Backup module control register in HP_SLEEP state                                              | 0x0084  | R/W    |
| PMU_HP_SLEEP_BACKUP_CLK_REG               | Backup flow ICG control register in HP_SLEEP state                                            | 0x0088  | R/W    |
| PMU_HP_SLEEP_SYSCLK_REG                   | System clock control register in HP_SLEEP state                                               | 0x008C  | R/W    |
| PMU_HP_SLEEP_HP_REGULATORO_REG            | HP sys regulator power control register in HP_SLEEP state                                     | 0x0090  | R/W    |
| PMU_HP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in HP_SLEEP state                                             | 0x0098  | R/W    |
| PMU_HP_SLEEP_LP_REGULATORO_REG            | LP sys regulator power control register in HP_SLEEP state                                     | 0x009C  | R/W    |
| PMU_HP_SLEEP_LP_DIG_POWER_REG             | LP system digital power domains control register in HP_SLEEP state                            | 0x00A8  | R/W    |
| PMU_HP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in HP_ACTIVE/HP_MODEM/HP_SLEEP state                  | 0x00AC  | R/W    |
| PMU_LP_SLEEP_LP_REGULATORO_REG            | LP sys regulator power control register in LP_SLEEP state                                     | 0x00B4  | R/W    |
| PMU_LP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in LP_SLEEP state                                             | 0x00BC  | R/W    |
| PMU_LP_SLEEP_LP_DIG_POWER_REG             | Digital power domain control register in LP_SLEEP state                                       | 0x00C0  | R/W    |
| PMU_LP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in LP_SLEEP state                                      | 0x00C4  | R/W    |
| PMU_POWER_PD_MEM_MASK_REG                 | Internal SRAMx domain force power up register                                                 | 0x0114  | R/W    |
```