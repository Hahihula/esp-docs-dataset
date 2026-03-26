

```markdown
| Name                                       | Description                                                                                      | Address | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|---------|--------|
| Configuration Registers                    |                                                                                                  |         |        |
| PMU_HP_ACTIVE_DIG_POWER_REG               | Digital power domain control register in HP_ACTIVE state                                        | 0x0000  | R/W    |
| PMU_HP_ACTIVE_ICG_HP_FUNC_REG             | HP system peripheral’s function clock control register in HP_ACTIVE state                       | 0x0004  | R/W    |
| PMU_HP_ACTIVE_HP_SYS_CNTL_REG             | System control register in HP_ACTIVE state                                                     | 0x0010  | R/W    |
| PMU_HP_ACTIVE_HP_CK_POWER_REG             | Clock source power control register in HP_ACTIVE state                                         | 0x0014  | R/W    |
| PMU_HP_ACTIVE_BIAS_REG                    | BIAS control register in HP_ACTIVE state                                                       | 0x0018  | R/W    |
| PMU_HP_ACTIVE_BACKUP_REG                  | Backup module control register in HP_ACTIVE state                                              | 0x001C  | R/W    |
| PMU_HP_ACTIVE_BACKUP_CLK_REG              | Backup module’s function clock control register in HP_ACTIVE state                              | 0x0020  | R/W    |
| PMU_HP_ACTIVE_SYSCLK_REG                  | System clock control register in HP_ACTIVE state                                               | 0x0024  | R/W    |
| PMU_HP_ACTIVE_HP_REGULATORO_REG           | Regulator power control register in HP_ACTIVE state                                            | 0x0028  | varies |
| PMU_HP_ACTIVE_XTAL_REG                    | XTAL_CLK power control register in HP_ACTIVE state                                             | 0x0030  | R/W    |
| PMU_HP_SLEEP_DIG_POWER_REG                | Digital power domain control register in HP_SLEEP state                                        | 0x0068  | R/W    |
| PMU_HP_SLEEP_ICG_HP_FUNC_REG              | HP system peripheral’s function clock control register in HP_SLEEP state                       | 0x006C  | R/W    |
| PMU_HP_SLEEP_HP_SYS_CNTL_REG              | System control register in HP_SLEEP state                                                      | 0x0078  | R/W    |
| PMU_HP_SLEEP_HP_CK_POWER_REG              | Clock source power control register in HP_SLEEP state                                          | 0x007C  | R/W    |
| PMU_HP_SLEEP_BIAS_REG                     | BIAS control register in HP_SLEEP state                                                        | 0x0080  | R/W    |
| PMU_HP_SLEEP_BACKUP_REG                   | Backup module control register in HP_SLEEP state                                               | 0x0084  | R/W    |
| PMU_HP_SLEEP_BACKUP_CLK_REG               | Backup module’s function clock control register in HP_SLEEP state                               | 0x0088  | R/W    |
| PMU_HP_SLEEP_SYSCLK_REG                   | System clock control register in HP_SLEEP state                                                | 0x008C  | R/W    |
| PMU_HP_SLEEP_HP_REGULATORO_REG            | Regulator power control register in HP_SLEEP state                                             | 0x0090  | R/W    |
```