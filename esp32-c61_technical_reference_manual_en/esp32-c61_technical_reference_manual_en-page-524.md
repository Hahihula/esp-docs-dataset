

```markdown
Chapter 11 Low-Power Management

Register 11.8. PMU_HP_ACTIVE_BACKUP_REG (0x001C)

Continued from the previous page...

PMU_HP_MODEM2ACTIVE_BACKUP_MODE Configures the backup direction and link list when PMU state switches from HP_MODEM to HP_ACTIVE. The configuration is the same as the register above. (R/W)

PMU_HP_SLEEP2ACTIVE_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_SLEEP to HP_ACTIVE.
0: Disable backup
1: Enable backup
(R/W)

PMU_HP_MODEM2ACTIVE_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_MODEM to HP_ACTIVE.
0: Disable backup
1: Enable backup
(R/W)

Register 11.9. PMU_HP_ACTIVE_BACKUP_CLK_REG (0x0020)
```