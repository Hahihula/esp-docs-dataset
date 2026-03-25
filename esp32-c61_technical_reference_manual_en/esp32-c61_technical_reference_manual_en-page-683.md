

```markdown
Register 16.3. HP_APM_REGIONn_ADDR_END_REG (n: 0-15) (0x0008+0xC*n)

HP_APM_REGIONn_ADDR_END

| 31 | 0 |
|----|---|
| Oxffffffff | Reset |

HP_APM_REGIONn_ADDR_END Configures the end address of region n. (R/W)


Register 16.4. HP_APM_REGIONn_ATTR_REG (n: 0-15) (0x000C+0xC*n)

(reserved)
HP_APM_REGIONn_RO_X
HP_APM_REGIONn_RO_W
HP_APM_REGIONn_RO_R
HP_APM_REGIONn_R1_X
HP_APM_REGIONn_R1_W
HP_APM_REGIONn_R1_R
HP_APM_REGIONn_R2_X
HP_APM_REGIONn_R2_W
HP_APM_REGIONn_R2_R
HP_APM_REGIONn_LOCK

| 31 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|----|----|----|----|---|---|---|---|---|---|---|---|---|---|
| 0 0 0 0 0 0 0 0 0 0 0 0 0 0 | Reset |

HP_APM_REGIONn_RO_X Configures the execution permission in region n in REEO mode. (R/W)
HP_APM_REGIONn_RO_W Configures the write permission in region n in REEO mode. (R/W)
HP_APM_REGIONn_RO_R Configures the read permission in region n in REEO mode. (R/W)
HP_APM_REGIONn_R1_X Configures the execution permission in region n in REE1 mode. (R/W)
HP_APM_REGIONn_R1_W Configures the write permission in region n in REE1 mode. (R/W)
HP_APM_REGIONn_R1_R Configures the read permission in region n in REE1 mode. (R/W)
HP_APM_REGIONn_R2_X Configures the execution permission in region n in REE2 mode. (R/W)
HP_APM_REGIONn_R2_W Configures the write permission in region n in REE2 mode. (R/W)
HP_APM_REGIONn_R2_R Configures the read permission in region n in REE2 mode. (R/W)

HP_APM_REGIONn_LOCK Configures to lock the value of region n configuration registers (HP_APM_REGIONn_ADDR_START_REG, HP_APM_REGIONn_ADDR_END_REG and HP_APM_REGIONn_ATTR_REG).
0: Do not lock
1: Lock
(R/W)
```