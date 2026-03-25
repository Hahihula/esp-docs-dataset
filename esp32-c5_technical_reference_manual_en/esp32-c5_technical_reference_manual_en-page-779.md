

```markdown
Register 18.47. LP_APMO_REGIONn_ADDR_END_REG (n: 0-7) (0x0008+0xC*n)

LP_APMO_REGIONn_ADDR_END

31 | 0
---|---
| 0xffffff | Reset

LP_APMO_REGIONn_ADDR_END Configures the end address of region n. (R/W)


Register 18.48. LP_APMO_REGIONn_ATTR_REG (n: 0-7) (0x000C+0xC*n)

(reserved) | LP_APMO_REGIONn_LOCK_R | LP_APMO_REGIONn_R2_W | LP_APMO_REGIONn_R2_X | LP_APMO_REGIONn_RO_R | LP_APMO_REGIONn_RO_X
---|---|---|---|---|---
31 | 12 | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0
| Reset

LP_APMO_REGIONn_RO_X Configures the execution permission in region n in REEO mode. (R/W)
LP_APMO_REGIONn_RO_W Configures the write permission in region n in REEO mode. (R/W)
LP_APMO_REGIONn_RO_R Configures the read permission in region n in REEO mode. (R/W)
LP_APMO_REGIONn_R1_X Configures the execution permission in region n in REE1 mode. (R/W)
LP_APMO_REGIONn_R1_W Configures the write permission in region n in REE1 mode. (R/W)
LP_APMO_REGIONn_R1_R Configures the read permission in region n in REE1 mode. (R/W)
LP_APMO_REGIONn_R2_X Configures the execution permission in region n in REE2 mode. (R/W)
LP_APMO_REGIONn_R2_W Configures the write permission in region n in REE2 mode. (R/W)
LP_APMO_REGIONn_R2_R Configures the read permission in region n in REE2 mode. (R/W)

LP_APMO_REGIONn_LOCK Configures to lock the value of region n configuration registers (LP_APMO_REGIONn_ADDR_START_REG, LP_APMO_REGIONn_ADDR_END_REG and LP_APMO_REGIONn_ATTR_REG).
0: Do not lock
1: Lock
(R/W)
```