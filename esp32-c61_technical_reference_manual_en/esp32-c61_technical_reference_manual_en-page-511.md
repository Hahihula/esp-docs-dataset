

```markdown
| Name                                       | Description                                                                                                                                              | Address   | Access |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|--------|
| PMU_HP_MODEM_ICG_HP_APB_REG               | Control register of HP system peripherals’ APB clocks in HP_MODEM state                                                                               | 0x003C    | R/W    |
| PMU_HP_MODEM_ICG_MODEM_REG                | Control register of HP system Modem clock gating in HP_MODEM state                                                                                     | 0x0040    | R/W    |
| PMU_HP_MODEM_HP_SYS_CNTL_REG              | System control register in HP_MODEM state                                                                                                                | 0x0044    | R/W    |
| PMU_HP_MODEM_HP_CK_POWER_REG              | Control register of clock source’s power in HP_MODEM state                                                                                              | 0x0048    | R/W    |
| PMU_HP_MODEM_BIAS_REG                     | Control register for the operating state of analog circuits (BIAS, DBG, CUR circuits) in HP_MODEM state                                                | 0x004C    | R/W    |
| PMU_HP_MODEM_BACKUP_REG                   | Data backup control register in HP_MODEM state                                                                                                         | 0x0050    | R/W    |
| PMU_HP_MODEM_BACKUP_CLK_REG               | Control register for the operating clocks of the backup module in HP_MODEM state                                                                       | 0x0054    | R/W    |
| PMU_HP_MODEM_SYSCLK_REG                   | Control register of the system clocks in HP_MODEM state                                                                                                | 0x0058    | R/W    |
| PMU_HP_MODEM_HP_REGULATORO_REG            | Control register of HP regulators’ power in HP_MODEM state, controlling all settings except drive                                                    | 0x005C    | R/W    |
| PMU_HP_MODEM_HP_REGULATOR1_REG            | Control register of HP regulators’ power in HP_MODEM state, controlling drive settings                                                                  | 0x0060    | R/W    |
| PMU_HP_MODEM_XTAL_REG                     | XTAL_CLK power control register in HP_MODEM state                                                                                                      | 0x0064    | R/W    |
| PMU_HP_SLEEP_DIG_POWER_REG                | Configuration register of digital power domains in HP_SLEEP state                                                                                        | 0x0068    | R/W    |
| PMU_HP_SLEEP_ICG_HP_FUNC_REG              | Control register of HP system peripherals’ function clocks in HP_SLEEP state                                                                          | 0x006C    | R/W    |
| PMU_HP_SLEEP_ICG_HP_APB_REG               | Control register of HP system peripherals’ APB clocks in HP_SLEEP state                                                                                | 0x0070    | R/W    |
| PMU_HP_SLEEP_ICG_MODEM_REG                | Control register of HP system Modem clock gating in HP_SLEEP state                                                                                     | 0x0074    | R/W    |
| PMU_HP_SLEEP_HP_SYS_CNTL_REG              | System control register in HP_SLEEP state                                                                                                               | 0x0078    | R/W    |
| PMU_HP_SLEEP_HP_CK_POWER_REG              | Control register of clock source’s power in HP_SLEEP state                                                                                              | 0x007C    | R/W    |
| PMU_HP_SLEEP_BIAS_REG                     | Control register for operation state of analog circuits (BIAS, DBG, CUR) in HP_SLEEP state                                                             | 0x0080    | R/W    |
| PMU_HP_SLEEP_BACKUP_REG                   | Data backup control register in HP_SLEEP state                                                                                                         | 0x0084    | R/W    |
```