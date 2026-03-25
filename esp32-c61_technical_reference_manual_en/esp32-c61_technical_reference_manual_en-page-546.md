

```markdown
|31|30|29|28|26|25|23|22|20|19|18|17|16|15|10|9|8|7|6|5|0|
|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
|0| | | | | | | | | | | | | | | | | | |Reset|
```

PMU_HP_MODDEM2SLEEP_BACKUP_MODEM_CLK_CODE Configures the ICG during backup process when PMU state switches from HP_MODDEM to HP_SLEEP. (R/W)

PMU_HP_ACTIVE2SLEEP_BACKUP_MODEM_CLK_CODE Configures the ICG during backup process when PMU state switches from HP_ACTIVE to HP_SLEEP. (R/W)

PMU_HP_MODDEM2SLEEP_BACKUP_CLK_SEL Configures the backup module’s function clock source when PMU state switches from HP_MODDEM to HP_SLEEP.
0: Select XTAL
1: Select PLL_CLK
2: Select RC_FAST_CLK
3: Invalid value
(R/W)

PMU_HP_ACTIVE2SLEEP_BACKUP_CLK_SEL Configures the backup module function clock source when PMU state switches from HP_ACTIVE to HP_SLEEP. The configuration is the same as the register above. (R/W)

PMU_HP_MODDEM2SLEEP_BACKUP_MODE Configures the backup direction and link list when PMU state switches switch from HP_MODDEM to HP_SLEEP.

Highest bit:
0: From peripheral to memory
1: From memory to peripheral

Lower two bits:
0: PAU_LINK_ADDR_0
1: PAU_LINK_ADDR_1
2: PAU_LINK_ADDR_2
3: PAU_LINK_ADDR_3
(R/W)

Continued on the next page...
```