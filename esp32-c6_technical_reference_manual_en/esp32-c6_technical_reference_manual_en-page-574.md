
```markdown
Register 16.4. HP_APM_REGIONn_ATTR_REG (n: 0-15) (0x000C+0xC*n)

| Bit 31 | ... | 11 | 10 | 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|--------|-----|-----|----|---|---|---|---|---|---|---|---|---|---|
|        |     |     |    |   |   |   |   |   |   |   |   |   | Reset |

HP_APM_REGIONn_RO_X      Configures the execution authority of REE_MODE 0 in region n. (R/W)
HP_APM_REGIONn_RO_W      Configures the write authority of REE_MODE 0 in region n. (R/W)
HP_APM_REGIONn_RO_R      Configures the read authority of REE_MODE 0 in region n. (R/W)
HP_APM_REGIONn_R1_X      Configures the execution authority of REE_MODE 1 in region n. (R/W)
HP_APM_REGIONn_R1_W      Configures the write authority of REE_MODE 1 in region n. (R/W)
HP_APM_REGIONn_R1_R      Configures the read authority of REE_MODE 1 in region n. (R/W)
HP_APM_REGIONn_R2_X      Configures the execution authority of REE_MODE 2 in region n. (R/W)
HP_APM_REGIONn_R2_W      Configures the write authority of REE_MODE 2 in region n. (R/W)
HP_APM_REGIONn_R2_R      Configures the read authority of REE_MODE 2 in region n. (R/W)

Register 16.5. HP_APM_FUNC_CTRL_REG (0x00C4)

| Bit 31 | ... | 4 | 3 | 2 | 1 | 0 |
|--------|-----|---|---|---|---|---|
|        |     |   |   |   | Reset |

HP_APM_MO_FUNC_EN    Configures to enable APM MO function. (R/W)
HP_APM_M1_FUNC_EN    Configures to enable APM M1 function. (R/W)
HP_APM_M2_FUNC_EN    Configures to enable APM M2 function. (R/W)
HP_APM_M3_FUNC_EN    Configures to enable APM M3 function. (R/W)
```