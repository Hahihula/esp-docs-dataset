

```markdown
| Bit | Field Name                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | PMU_HP_SLEEP2MODEM_BACKUP_EN                                              |
| 29  | (reserved)                                                                  |
| 28  | PMU_HP_SLEEP2MODEM_BACKUP_MODE                                           |
| 27  | (reserved)                                                                  |
| 26  | PMU_HP_SLEEP2MODEM_BACKUP_CLK_SEL                                        |
| 25  | (reserved)                                                                  |
| 24  | PMU_HP_SLEEP2MODEM_BACKUP_MODE                                           |
| 23  | (reserved)                                                                  |
| 22  | PMU_HP_SLEEP2MODEM_BACKUP_CLK_CODE                                      |
| 21  | (reserved)                                                                  |
| 20  | PMU_HP_SLEEP2MODEM_BACKUP_MODE                                           |
| 19  | (reserved)                                                                  |
| 18  | PMU_HP_SLEEP2MODEM_BACKUP_CLK_SEL                                       |
| 17  | (reserved)                                                                  |
| 16  | PMU_HP_SLEEP2MODEM_BACKUP_MODE                                           |
| 15  | (reserved)                                                                  |
| 14  | PMU_HP_SLEEP2MODEM_BACKUP_CLK_CODE                                      |
| 13  | (reserved)                                                                  |
| 12  | PMU_HP_SLEEP2MODEM_BACKUP_MODE                                           |
| 11  | (reserved)                                                                  |
| 10  | PMU_HP_SLEEP2MODEM_BACKUP_CLK_SEL                                       |
| 9   | (reserved)                                                                  |
| 8   | PMU_HP_SLEEP2MODEM_BACKUP_MODE                                           |
| 7   | (reserved)                                                                  |
| 6   | PMU_HP_SLEEP2MODEM_BACKUP_CLK_CODE                                      |
| 5   | (reserved)                                                                  |
| 4   | PMU_HP_SLEEP2MODEM_BACKUP_MODE                                           |
| 3   | (reserved)                                                                  |
| 2   | PMU_HP_SLEEP2MODEM_BACKUP_CLK_SEL                                       |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                      |
```

PMU_HP_SLEEP2MODEM_BACKUP_MODEN_CLK_CODE Configures the ICG during backup process when PMU state switches from HP_SLEEP to HP_MODEM. (R/W)

PMU_HP_SLEEP2MODEM_BACKUP_CLK_SEL Configures the backup module’s function clock source when PMU state switches from HP_SLEEP to HP_MODEM.
0: Select XTAL
1: Select PLL_CLK
2: Select RC_FAST_CLK
3: Invalid value
(R/W)

PMU_HP_SLEEP2MODEM_BACKUP_MODE Configures the backup direction and link list when PMU state switches switch from HP_SLEEP to HP_MODEM.
Highest bit:
0: From peripheral to memory
1: From memory to peripheral
Lower two bits:
0: PAU_LINK_ADDR_0
1: PAU_LINK_ADDR_1
2: PAU_LINK_ADDR_2
3: PAU_LINK_ADDR_3
(R/W)

PMU_HP_SLEEP2MODEM_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_SLEEP to HP_MODEM.
0: Disable backup
1: Enable backup
(R/W)
```