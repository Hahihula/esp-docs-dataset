

```markdown
Register 11.16. PMU_HP_SLEEP_BACKUP_REG (0x0084)

| Bit | 31 | 30 | 29 | 28 | 26 | 25 | 23 | 22 | 20 | 19 | 18 | 17 | 16 | 15 | 10 | 9 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|
|     |    | PMU_HP_ACTIVE2SLEEP_BACKUP_EN (reserved) | O | O | O | O | O | O | O | O | O | O | O | O | Reset |

PMU_HP_ACTIVE2SLEEP_BACKUP_CLK_SEL Configures the backup module function clock source when PMU state switches from HP_ACTIVE to HP_SLEEP.
0: Select XTAL
1: Select PLL_CLK
2: Select RC_FAST_CLK
3: Invalid value
(R/W)

PMU_HP_ACTIVE2SLEEP_BACKUP_MODE Configures the backup direction and link list when PMU state switches from HP_ACTIVE to HP_SLEEP.
Highest bit:
0: From memory to peripheral
1: From peripheral to memory
Lower two bits:
0: PAU_LINK_ADDR_0
1: PAU_LINK_ADDR_1
2: PAU_LINK_ADDR_2
3: PAU_LINK_ADDR_3
(R/W)

PMU_HP_ACTIVE2SLEEP_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_ACTIVE to HP_SLEEP.
0: Disable backup
1: Enable backup
(R/W)
```