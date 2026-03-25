

```markdown
Register 16.40. CPU_APM_REGIONn_ATTR_REG (n: 0-7) (0x000C+0xC*n)

| 31 | 30 | 29 | 28 | 27 | 26 | 25 | 24 | 23 | 22 | 21 | 20 | 19 | 18 | 17 | 16 | 15 | 14 | 13 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|
| 0   | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | Reset |

CPU_APM_REGIONn_RO_X Configures the execution permission in region n in REEO mode. (R/W)

CPU_APM_REGIONn_RO_W Configures the write permission in region n in REEO mode. (R/W)

CPU_APM_REGIONn_RO_R Configures the read permission in region n in REEO mode. (R/W)

CPU_APM_REGIONn_R1_X Configures the execution permission in region n in REE1 mode. (R/W)

CPU_APM_REGIONn_R1_W Configures the write permission in region n in REE1 mode. (R/W)

CPU_APM_REGIONn_R1_R Configures the read permission in region n in REE1 mode. (R/W)

CPU_APM_REGIONn_R2_X Configures the execution permission in region n in REE2 mode. (R/W)

CPU_APM_REGIONn_R2_W Configures the write permission in region n in REE2 mode. (R/W)

CPU_APM_REGIONn_R2_R Configures the read permission in region n in REE2 mode. (R/W)

CPU_APM_REGIONn_LOCK Configures to lock the value of region n's configuration registers (CPU_APM_REGIONn_ADDR_START_REG, CPU_APM_REGIONn_ADDR_END_REG, and CPU_APM_REGIONn_ATTR_REG).

0: Do not lock
1: Lock
(R/W)
```