

```markdown
Register 18.3. HP_APM_REGIONn_ADDR_END_REG (n: 0-15) (0x0008+0xC*n)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | 0                                                                             |
|     |                             | Reset                                                                        |
|     |                             | 0xffffffff                                                                  |

HP_APM_REGIONn_ADDR_END Configures the end address of region n. (R/W)

Register 18.4. HP_APM_REGIONn_ATTR_REG (n: 0-15) (0x000C+0xC*n)

| Bit | Field Name                  | Description                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 31  |                             | (reserved)                                                                   |
|     |                             |                                                                             |
| 12  | HP_APM_REGIONn_RO_X         | Configures the execution permission in region n in REEO mode. (R/W)          |
| 11  | HP_APM_REGIONn_RO_W         | Configures the write permission in region n in REEO mode. (R/W)              |
| 10  | HP_APM_REGIONn_RO_R         | Configures the read permission in region n in REEO mode. (R/W)               |
| 9   | HP_APM_REGIONn_R1_X         | Configures the execution permission in region n in REE1 mode. (R/W)          |
| 8   | HP_APM_REGIONn_R1_W         | Configures the write permission in region n in REE1 mode. (R/W)              |
| 7   | HP_APM_REGIONn_R1_R         | Configures the read permission in region n in REE1 mode. (R/W)               |
| 6   | HP_APM_REGIONn_R2_X         | Configures the execution permission in region n in REE2 mode. (R/W)          |
| 5   | HP_APM_REGIONn_R2_W         | Configures the write permission in region n in REE2 mode. (R/W)              |
| 4   | HP_APM_REGIONn_R2_R         | Configures the read permission in region n in REE2 mode. (R/W)               |
| 3   | HP_APM_REGIONn_LOCK         | Configures to lock the value of region n configuration registers (HP_APM_REGIONn_ADDR_START_REG, HP_APM_REGIONn_ADDR_END_REG and HP_APM_REGIONn_ATTR_REG).<br>0: Do not lock<br>1: Lock (R/W)
```