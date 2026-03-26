

```markdown
## Register 8.37. EFUSE_WR_TIM_CONF0_RS_BYPASS_REG (0x01F8)

| Bit Range | Field Name                          | Description                                                                 |
|-----------|--------------------------------------|-----------------------------------------------------------------------------|
| 21:20     | —                                    | (reserved)                                                                  |
| 19        | EFUSE_BYPASS_RS_CORRECTION           | Configures whether to bypass the Reed-Solomon (RS) correction step.         |
|           | O: Not bypass                        | 1: Bypass                                                                   |
|           | (R/W)                                |                                                                             |
| 18        | EFUSE_BYPASS_RS_BLK_NUM              | Configures which block number to bypass the Reed-Solomon (RS) correction step. (R/W) |
| 17        | EFUSE_UPDATE                         | Configures whether to update multi-bit register signals.                    |
|           | 1: Update                            | 0: No effect                                                                |
|           | (WT)                                 |                                                                             |
| 16-15     | EFUSE_TPGM_INACTIVE                  | Configures the inactive programming time. Measurement unit: One cycle of the eFuse core clock. (R/W) |

## Register 8.38. EFUSE_STATUS_REG (0x01D0)

| Bit Range | Field Name                          | Description                                                                 |
|-----------|--------------------------------------|-----------------------------------------------------------------------------|
| 24-25     | —                                    | (reserved)                                                                  |
| 23        | EFUSE_STATE                          | Represents the state of the eFuse state machine.                            |
|           | O: Reset state, the initial state after power-up                              |
|           | 1: Idle state                                                                          |
|           | Other values: Non-idle state                                                         |
|           | (RO)                                                                                   |
| 22-19     | EFUSE_CUR_ECDSA_BLK                  | Represents which block is used for ECDSA key output. (RO)                    |
| 20        | EFUSE_BLK0_VALID_BIT_CNT             | Represents the number of block valid bit. (RO)                               |
```