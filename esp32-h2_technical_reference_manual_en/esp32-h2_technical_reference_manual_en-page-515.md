

```markdown
Register 15.4. HP_APM_REGIONn_ATTR_REG (n: 0-15) (0x000C+0xC*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | HP_APM_REGIONn_RO_X                                                         | Configures the execution permission in region n in REEO mode. (R/W)        |
| 29  | HP_APM_REGIONn_RO_W                                                         | Configures the write permission in region n in REEO mode. (R/W)             |
| 28  | HP_APM_REGIONn_RO_R                                                         | Configures the read permission in region n in REEO mode. (R/W)              |
| 27  | HP_APM_REGIONn_R1_X                                                         | Configures the execution permission in region n in REE1 mode. (R/W)          |
| 26  | HP_APM_REGIONn_R1_W                                                         | Configures the write permission in region n in REE1 mode. (R/W)             |
| 25  | HP_APM_REGIONn_R1_R                                                         | Configures the read permission in region n in REE1 mode. (R/W)              |
| 24  | HP_APM_REGIONn_R2_X                                                         | Configures the execution permission in region n in REE2 mode. (R/W)          |
| 23  | HP_APM_REGIONn_R2_W                                                         | Configures the write permission in region n in REE2 mode. (R/W)             |
| 22  | HP_APM_REGIONn_R2_R                                                         | Configures the read permission in region n in REE2 mode. (R/W)              |

Register 15.5. HP_APM_FUNC_CTRL_REG (0x00C4)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | Reset                                                                      |
| 29  | HP_APM_M0_FUNC_EN                                                          | Configures to enable permission management for HP_APM_CTRL M0. (R/W)        |
| 28  | HP_APM_M1_FUNC_EN                                                          | Configures to enable permission management for HP_APM_CTRL M1. (R/W)        |
| 27  | HP_APM_M2_FUNC_EN                                                          | Configures to enable permission management for HP_APM_CTRL M2. (R/W)        |
| 26  | HP_APM_M3_FUNC_EN                                                          | Configures to enable permission management for HP_APM_CTRL M3. (R/W)        |
```