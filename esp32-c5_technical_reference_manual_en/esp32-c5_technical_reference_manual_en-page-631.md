

```markdown
Register 13.16. PMU_HP_MODEM_BACKUP_REG (0x0050)

| Bit | 31 | 30 | 29 | 28 | 25 | 24 | 20 | 19 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 6 | 5 | 4 | 3 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|
|     | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0 | 0 | 0 | 0 | 0 | Reset |

PMU_HP_SLEEP2MODEM_BACKUP_CLK_SEL Configures the backup module's function clock source when PMU state switches from HP_SLEEP to HP_MODEM.
- O: Select XTAL
- 1: Select PLL_CLK
- 2: Select RC_FAST_CLK
- 3: Invalid value (R/W)

PMU_HP_SLEEP2MODEM_BACKUP_MODE Configures the backup direction and link list when PMU state switches switch from HP_SLEEP to HP_MODEM.
Highest bit:
- O: From peripheral to memory
- 1: From memory to peripheral
Lower four bits: Select a linked list pointer. The pointer is set within the linked list. (R/W)

PMU_HP_SLEEP2MODEM_BACKUP_EN Configures whether to enable the backup flow when PMU state switches from HP_SLEEP to HP_MODEM.
- O: Disable backup
- 1: Enable backup (R/W)
```