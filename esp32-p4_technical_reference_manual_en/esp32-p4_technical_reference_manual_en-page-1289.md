

```markdown
## Register 20.54. HP_SYSTEM_HP_RNG_CFG_REG (0x01D8)

| Bit Range | Field Name                          | Description                                                                 |
|-----------|--------------------------------------|-----------------------------------------------------------------------------|
| 31-24     | HP_SYSTEM_RNG_SAMPLE_CNT            | Represents the RNG sample count for debugging. (RO)                         |
| 23        | HP_SYSTEM_RNG_CHAIN_CLK_DIV_NUM     | Configures the chain clock division number for debugging. (R/W)             |
| 15        | HP_SYSTEM_RNG_SAMPLE_ENABLE          | Configures whether or not to enable the RNG sample chain.<br>0: Disable<br>1: Enable<br>(R/W) |

### Field Descriptions

- **HP_SYSTEM_RNG_SAMPLE_ENABLE**: Configures whether or not to enable the RNG sample chain.
  - 0: Disable
  - 1: Enable
  - (R/W)

- **HP_SYSTEM_RNG_CHAIN_CLK_DIV_NUM**: Configures the chain clock division number for debugging. (R/W)

- **HP_SYSTEM_RNG_SAMPLE_CNT**: Represents the RNG sample count for debugging. (RO)


## Register 20.55. HP_SYSTEM_HP_UART_PD_CTRL_REG (0x01DC)

| Bit Range | Field Name                          | Description                                                                 |
|-----------|--------------------------------------|-----------------------------------------------------------------------------|
| 31-2       | reserved                             |                                                                             |
| 1         | HP_SYSTEM_UART_MEM_FORCE_PD          | Configures whether or not to force power down HP UART internal memory.<br>0: No effect<br>1: Power down<br>(R/W) |
| 0         | HP_SYSTEM_UART_MEM_FORCE_PU          | Configures whether or not to force power up HP UART internal memory.<br>0: No effect<br>1: Power up<br>(R/W) |

### Field Descriptions

- **HP_SYSTEM_UART_MEM_FORCE_PD**: Configures whether or not to force power down HP UART internal memory.
  - 0: No effect
  - 1: Power down
  - (R/W)

- **HP_SYSTEM_UART_MEM_FORCE_PU**: Configures whether or not to force power up HP UART internal memory.
  - 0: No effect
  - 1: Power up
  - (R/W)
```