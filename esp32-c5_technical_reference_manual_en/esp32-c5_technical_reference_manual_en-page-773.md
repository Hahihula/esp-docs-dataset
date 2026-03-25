

```markdown
Register 18.31. LP_APM_REGIONn_ADDR_END_REG (n: 0-7) (0x0008+0xC*n)

LP_APM_REGIONn_ADDR_END

LP_APM_REGIONn_ADDR_END Configures the end address of region n. (R/W)


Register 18.32. LP_APM_REGIONn_ATTR_REG (n: 0-7) (0x000C+0xC*n)

(reserved)
LP_APM_REGIONn_RO_X
LP_APM_REGIONn_RO_W
LP_APM_REGIONn_RO_R
LP_APM_REGIONn_R1_X
LP_APM_REGIONn_R1_W
LP_APM_REGIONn_R1_R
LP_APM_REGIONn_R2_X
LP_APM_REGIONn_R2_W
LP_APM_REGIONn_R2_R
LP_APM_REGIONn_LOCK

LP_APM_REGIONn_RO_X Configures the execution permission in region n in REEO mode. (R/W)
LP_APM_REGIONn_RO_W Configures the write permission in region n in REEO mode. (R/W)
LP_APM_REGIONn_RO_R Configures the read permission in region n in REEO mode. (R/W)
LP_APM_REGIONn_R1_X Configures the execution permission in region n in REE1 mode. (R/W)
LP_APM_REGIONn_R1_W Configures the write permission in region n in REE1 mode. (R/W)
LP_APM_REGIONn_R1_R Configures the read permission in region n in REE1 mode. (R/W)
LP_APM_REGIONn_R2_X Configures the execution permission in region n in REE2 mode. (R/W)
LP_APM_REGIONn_R2_W Configures the write permission in region n in REE2 mode. (R/W)
LP_APM_REGIONn_R2_R Configures the read permission in region n in REE2 mode. (R/W)

LP_APM_REGIONn_LOCK Configures to lock the value of region n configuration registers (LP_APM_REGIONn_ADDR_START_REG, LP_APM_REGIONn_ADDR_END_REG and LP_APM_REGIONn_ATTR_REG).
0: Do not lock
1: Lock
(R/W)
```