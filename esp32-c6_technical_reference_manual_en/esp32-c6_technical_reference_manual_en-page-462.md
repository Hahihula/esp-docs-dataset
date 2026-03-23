

```markdown
Chapter 12 Low-Power Management

Register 12.26. PMU_HP_SLEEP_BACKUP_REG (0x0084)

Continued from the previous page...

PMU_HP_ACTIVE2SLEEP_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_ACTIVE to HP_SLEEP.
O: Disable backup
1: Enable backup
(R/W)

Register 12.27. PMU_HP_SLEEP_BACKUP_CLK_REG (0x0088)

PMU_HP_SLEEP_BACKUP_ICG_FUNC_EN Configures whether to enable each peripheral's function clock when the target state is HP_SLEEP. For details, please refer to Chapter 8 Reset and Clock.
O: Disable
1: Enable
(R/W)
```