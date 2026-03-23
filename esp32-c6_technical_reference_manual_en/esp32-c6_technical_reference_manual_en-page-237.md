

```markdown
## Register 6.103. EFUSE_CLK_REG (0x01C8)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 17  | EFUSE_CLK_EN                   | Configures whether or not to force enable eFuse register configuration clock signal. <br> 1: Force <br> 0: The clock is enabled only during the reading and writing of registers (R/W) |
| 3   | EFUSE_MEM_FORCE_PD             | Configures whether or not to force eFuse SRAM into power-saving mode. <br> 1: Force <br> 0: No effect (R/W) |
| 2   | EFUSE_MEM_CLK_FORCE_ON         | Configures whether or not to force activate clock signal of eFuse SRAM. <br> 1: Force activate <br> 0: No effect (R/W) |
| 1   | EFUSE_MEM_FORCE_PU             | Configures whether or not to force eFuse SRAM into working mode. <br> 1: Force <br> 0: No effect (R/W) |
| 0   |                                | Reset                                                                       |

## Register 6.104. EFUSE_CONF_REG (0x01CC)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  |                                | (reserved)                                                                  |
| 15  | EFUSE_OP_CODE                  | Configures operation command type. <br> 0x5A5A: Programming operation command <br> 0x5AA5: Read operation command <br> Other values: No effect (R/W) |
```