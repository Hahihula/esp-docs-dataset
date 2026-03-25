

```markdown
Chapter 11 Low-Power Management

Register 11.34. PMU_HP_SLEEP_BACKUP_REG (0x0084)

Continued from the previous page...

PMU_HP_ACTIVE2SLEEP_BACKUP_MODE Configures the backup direction and link list when PMU state switches from HP_ACTIVE to HP_MODDEM. The configuration is the same as the register above. (R/W)

PMU_HP_MODEM2SLEEP_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_MODDEM to HP_SLEEP.
0: Disable backup
1: Enable backup
(R/W)

PMU_HP_ACTIVE2SLEEP_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_ACTIVE to HP_SLEEP.
0: Disable backup
1: Enable backup
(R/W)

Register 11.35. PMU_HP_SLEEP_BACKUP_CLK_REG (0x0088)
```
```markdown
| 31 | 0 |
|----|---|
|    |   |
|    | Reset |

PMU_HP_SLEEP_BACKUP_ICG_FUNC_EN Configures whether to enable each peripherals' function clock when the target state is HP_SLEEP. For details, please refer to Chapter 7 Reset and Clock.
0: Disable
1: Enable
(R/W)
```