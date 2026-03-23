

```markdown
Register 12.6. PMU_HP_ACTIVE_BACKUP_REG (0x001C)

| Bit | 31 | 30 | 29 | 28 | 26 | 25 | 23 | 22 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 8 | 7 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0 | 0 | 0 |
|     |    | (reserved) | PMU_HP_SLEEP2ACTIVE_BACKUP_EN | (reserved) | PMU_HP_MODEM2ACTIVE_BACKUP_EN | PMU_HP_SLEEP2ACTIVE_BACKUP_CLK_SEL | PMU_HP_MODEM2ACTIVE_BACKUP_CLK_SEL | PMU_HP_SLEEP2ACTIVE_BACKUP_MODE | (reserved) | PMU_HP_MODEM2ACTIVE_BACKUP_MODE | PMU_HP_SLEEP2ACTIVE_BACKUP_CLK_SEL | (reserved) |

PMU_HP_SLEEP2ACTIVE_BACKUP_CLK_SEL Configures the backup module’s function clock source when PMU state switches from HP_SLEEP to HP_ACTIVE.
0: Select XTAL
1: Select PLL_CLK
2: Select RC_FAST_CLK
3: Invalid value
(R/W)

PMU_HP_MODEM2ACTIVE_BACKUP_CLK_SEL Configures the backup module’s function clock source when PMU state switches from HP_MODEM to HP_ACTIVE. The configuration is the same as the register above. (R/W)

PMU_HP_SLEEP2ACTIVE_BACKUP_MODE Configures the backup direction and link list when PMU state switches switch from HP_SLEEP to HP_ACTIVE.
Highest bit:
0: From peripheral to memory
1: From memory to peripheral
Lower two bits:
0: PAU_LINK_ADDR_0
1: PAU_LINK_ADDR_1
2: PAU_LINK_ADDR_2
3: PAU_LINK_ADDR_3
(R/W)

PMU_HP_MODEM2ACTIVE_BACKUP_MODE Configures the backup direction and link list when PMU state switches from HP_MODEM to HP_ACTIVE. The configuration is the same as the register above. (R/W)

PMU_HP_SLEEP2ACTIVE_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_SLEEP to HP_ACTIVE.
0: Disable backup
1: Enable backup
(R/W)
```