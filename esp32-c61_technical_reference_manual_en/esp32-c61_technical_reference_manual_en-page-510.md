

```markdown
| Name                                       | Description                                                                                      | Address   | Access |
|--------------------------------------------|--------------------------------------------------------------------------------------------------|-----------|--------|
| PMU_HP_ACTIVE_DIG_POWER_REG               | Configuration register of digital power domains in HP_ACTIVE state                               | 0x0000    | R/W    |
| PMU_HP_ACTIVE_ICG_HP_FUNC_REG             | Control register of HP system peripherals’ function clocks in HP_ACTIVE state                   | 0x0004    | R/W    |
| PMU_HP_ACTIVE_ICG_HP_APP_REG              | Control register of HP system peripherals’ APB clocks in HP_ACTIVE state                        | 0x0008    | R/W    |
| PMU_HP_ACTIVE_ICG_MODEM_REG               | Control register of HP system Modem clock gating in HP_ACTIVE state                             | 0x000C    | R/W    |
| PMU_HP_ACTIVE_HP_SYS_CNTL_REG             | System control register in HP_ACTIVE state                                                     | 0x0010    | R/W    |
| PMU_HP_ACTIVE_HP_CK_POWER_REG             | Control register of clock source’s power in HP_ACTIVE state                                     | 0x0014    | R/W    |
| PMU_HP_ACTIVE_BIAS_REG                    | Control register for the operating state of analog circuits (BIAS, DBG, CUR circuits) in HP_ACTIVE state | 0x0018    | R/W    |
| PMU_HP_ACTIVE_BACKUP_REG                  | Data backup control register in HP_ACTIVE state                                                | 0x001C    | R/W    |
| PMU_HP_ACTIVE_BACKUP_CLK_REG              | Control register for the operating clocks of the backup module in HP_ACTIVE state                | 0x0020    | R/W    |
| PMU_HP_ACTIVE_SYSCLK_REG                  | Control register of the system clocks in HP_ACTIVE state                                        | 0x0024    | R/W    |
| PMU_HP_ACTIVE_HP_REGULATOR0_REG           | Control register of HP regulators’ power in HP_ACTIVE state, controlling all settings except drive | 0x0028    | varies |
| PMU_HP_ACTIVE_HP_REGULATOR1_REG           | Control register of HP regulators’ power in HP_ACTIVE state, controlling drive settings         | 0x002C    | R/W    |
| PMU_HP_ACTIVE_XTAL_REG                    | XTAL_CLK power control register in HP_ACTIVE state                                              | 0x0030    | R/W    |
| PMU_HP_MODEM_DIG_POWER_REG                | Configuration register of digital power domains in HP_MODEM state                               | 0x0034    | R/W    |
| PMU_HP_MODEM_ICG_HP_FUNC_REG              | Control register of HP system peripherals’ function clocks in HP_MODEM state                    | 0x0038    | R/W    |
```