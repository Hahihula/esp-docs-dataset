

```markdown
| Name                                       | Description                                                                                                                                              | Address | Access |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------|--------|
| PMU_HP_SLEEP_BACKUP_CLK_REG               | Control register for the operating clocks of the backup module in HP_SLEEP state                                                                       | 0x0088  | R/W    |
| PMU_HP_SLEEP_SYSCLK_REG                   | Control register of the system clocks in HP_SLEEP state                                                                                                | 0x008C  | R/W    |
| PMU_HP_SLEEP_HP_REGULATOR0_REG            | Control register of HP regulators’ power in HP_SLEEP state, controlling all settings except drive                                                       | 0x0090  | R/W    |
| PMU_HP_SLEEP_HP_REGULATOR1_REG            | Control register of HP regulators’ power in HP_SLEEP state, controlling drive settings                                                                  | 0x0094  | R/W    |
| PMU_HP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in HP_SLEEP state                                                                                                       | 0x0098  | R/W    |
| PMU_HP_SLEEP_LP_REGULATOR0_REG            | LP regulator power control register in HP_SLEEP state, controlling all settings except drive                                                             | 0x009C  | R/W    |
| PMU_HP_SLEEP_LP_REGULATOR1_REG            | LP regulator power control register in HP_SLEEP state, controlling drive settings                                                                      | 0x00A0  | R/W    |
| PMU_HP_SLEEP_LP_DIG_POWER_REG             | Configuration register of digital power domains in LP system in HP_SLEEP state                                                                         | 0x00A8  | R/W    |
| PMU_HP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in HP_ACTIVE, HP_MODEM and HP_SLEEP states                                                                       | 0x00AC  | R/W    |
| PMU_LP_SLEEP_LP_REGULATOR0_REG            | LP regulator power control register in LP_SLEEP state, controlling all settings except drive                                                             | 0x00B4  | R/W    |
| PMU_LP_SLEEP_LP_REGULATOR1_REG            | LP regulator power control register in LP_SLEEP state, controlling drive settings                                                                      | 0x00B8  | R/W    |
| PMU_LP_SLEEP_XTAL_REG                     | XTAL_CLK power control register in LP_SLEEP state                                                                                                       | 0x00BC  | R/W    |
| PMU_LP_SLEEP_LP_DIG_POWER_REG             | Configuration register of digital power domains in LP system in LP_SLEEP state                                                                         | 0x00C0  | R/W    |
| PMU_LP_SLEEP_LP_CK_POWER_REG              | Low-speed clock power control register in LP_SLEEP state                                                                                               | 0x00C4  | R/W    |
| PMU_LP_SLEEP_BIAS_REG                     | Control register for operation state of analog circuits (BIAS, DBG, CUR) in LP_SLEEP state                                                               | 0x00C8  | R/W    |
| PMU_IMM_HP_CK_POWER_REG                   | Software-controlled enable signal for HP clock power on/off                                                                                             | 0x00CC  | WT     |
```