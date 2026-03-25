

```markdown
Chapter 5 eFuse Controller (EFUSE)                                                                 GoBack


Register 5.32. EFUSE_CLK_REG (0x01C8)

| Bit | Description                        |
|-----|------------------------------------|
| 31  | (reserved)                         |
| 17  | EFUSE_CLK_EN                       |
| 16  | (reserved)                         |
| 3   | EFUSE_MEM_FORCE_PU                 |
| 2   | EFUSE_MEM_CLK_FORCE_ON             |
| 1   | EFUSE_MEM_FORCE_PD                 |
| 0   | Reset                              |

EFUSE_MEM_FORCE_PD Configures whether to force eFuse SRAM into power-saving mode.
- 1: Force
- 0: No effect
(R/W)

EFUSE_MEM_CLK_FORCE_ON Configures whether to force activate clock signal of eFuse SRAM.
- 1: Force activate
- 0: No effect
(R/W)

EFUSE_MEM_FORCE_PU Configures whether to force eFuse SRAM into working mode.
- 1: Force
- 0: No effect
(R/W)

EFUSE_CLK_EN Configures whether to force enable eFuse register configuration clock signal.
- 1: Force
- 0: The clock is enabled only during the reading and writing of registers
(R/W)


Register 5.33. EFUSE_CONF_REG (0x01CC)

| Bit | Description                        |
|-----|------------------------------------|
| 31  | (reserved)                         |
| 20  | EFUSE_CFG_ECDSA_BLK                |
| 19  | (reserved)                         |
| 16  | (reserved)                         |
| 15  | EFUSE_OP_CODE                      |
| 0   | Reset                              |

EFUSE_OP_CODE Configures operation command type.
- 0x5A5A: Programming operation command
- 0x5AA5: Read operation command
Other values: No effect
(R/W)

EFUSE_CFG_ECDSA_BLK Configures which block to use for ECDSA key output. (R/W)
```