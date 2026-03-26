

```markdown
Chapter 8 eFuse Controller (EFUSE) GoBack


Register 8.31. EFUSE_CLK_REG (0x01C8)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 17  | EFUSE_CLK_EN                   | Configures whether to force enable eFuse register configuration clock signal. |
|     |                                | 1: Force                                                                      |
|     |                                | 0: The clock is enabled only during the reading and writing of registers      |
| (R/W)|                                 |                                                                             |

EFUSE_MEM_FORCE_PD Configures whether to force power down eFuse SRAM.
1: Force
0: No effect
(R/W)

EFUSE_MEM_CLK_FORCE_ON Configures whether to force activate clock signal of eFuse SRAM.
1: Force activate
0: No effect
(R/W)

EFUSE_MEM_FORCE_PU Configures whether to force power up eFuse SRAM.
1: Force
0: No effect
(R/W)


Register 8.32. EFUSE_CONF_REG (0x01CC)

| Bit | Field Name                     | Description                                                                 |
|-----|---------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                     |                                                                             |
| 20  | EFUSE_CFG_ECDSA_BLK            | Configures which block to use for ECDSA key output. (R/W)                    |
|     |                                 | 0x5A5A: Program operation command                                           |
|     |                                 | 0x5AA5: Read operation command                                              |
|     |                                 | Other values: No effect                                                     |
| (R/W)|                                 |                                                                             |

EFUSE_OP_CODE Configures operation command type.
```

*Note: The provided text includes register bit fields, descriptions, and configuration details for EFUSE_CLK_REG and EFUSE_CONF_REG registers. Diagrams are referenced but not included in the extracted Markdown due to limitations; however, their structure is described via table formatting as per standard markdown conventions.*