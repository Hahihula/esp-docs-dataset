

```markdown
Register 16.28. LP_APM_REGIONn_ATTR_REG (n: 0-3) (0x000C+0xC*n)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | LP_APM_REGIONn_R2_W                                                         | Configures the write authority of REE_MODE 2 in region n. (R/W)             |
| 29  | LP_APM_REGIONn_R2_X                                                         | Configures the execution authority of REE_MODE 2 in region n. (R/W)          |
| 28  | LP_APM_REGIONn_R1_W                                                         | Configures the write authority of REE_MODE 1 in region n. (R/W)             |
| 27  | LP_APM_REGIONn_R1_X                                                         | Configures the execution authority of REE_MODE 1 in region n. (R/W)          |
| 26  | LP_APM_REGIONn_R1_R                                                         | Configures the read authority of REE_MODE 1 in region n. (R/W)               |
| 25  | LP_APM_REGIONn_RO_W                                                         | Configures the write authority of REE_MODE 0 in region n. (R/W)             |
| 24  | LP_APM_REGIONn_RO_X                                                         | Configures the execution authority of REE_MODE 0 in region n. (R/W)          |
| 23  | LP_APM_REGIONn_RO_R                                                         | Configures the read authority of REE_MODE 0 in region n. (R/W)               |

Register 16.29. LP_APM_FUNC_CTRL_REG (0x00C4)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 30  | LP_APM_M0_FUNC_EN                                                           | Configures APM M0 function enable. (R/W)                                    |
| 29  | LP_APM_M1_FUNC_EN                                                           | Configures APM M1 function enable. (R/W)                                    |
```