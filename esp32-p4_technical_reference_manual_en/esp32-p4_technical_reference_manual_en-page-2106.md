

```markdown
## 41.8 Registers

The addresses in this section are relative to VAD base address provided in Table 7.3-2 in Chapter 7 System and Memory.

For how to program reserved fields, please refer to Section Programming Reserved Register Field.

### Register 41.1. LP_I2S_VAD_CONF_REG (0x0000)

| Bit | Description                     |
|-----|----------------------------------|
| 3   | LP_I2S_VAD_FORCE_START          |
| 2   | LP_I2S_VAD_RESET                |
| 1   | LP_I2S_VAD_EN                   |
| 0   | Reset                           |

LP_I2S_VAD_EN Configures whether to enable the automatic operation mode.
- 0: Disable
- 1: Enable
(R/W)

LP_I2S_VAD_RESET Configures whether to reset the VAD module.
- 0: Not reset
- 1: Reset
(WT)

LP_I2S_VAD_FORCE_START Configures whether to trigger the manual operation on one frame of data.
- 0: Not trigger
- 1: Trigger
(WT)

### Register 41.2. LP_I2S_VAD_RESULT_REG (0x0004)

| Bit | Description                     |
|-----|----------------------------------|
| 3   | LP_I2S_ENERGY_ENOUGH            |
| 2   | LP_I2S_VAD_FLAG                 |
| 1   | Reset                           |
| 0   | Reserved                        |

LP_I2S_VAD_FLAG Represents the voice activity status. For details, see Section 41.4.1. (RO)

LP_I2S_ENERGY_ENOUGH Represents whether the current frame passes the energy threshold check. For details, see Section 41.4.1. (RO)
```