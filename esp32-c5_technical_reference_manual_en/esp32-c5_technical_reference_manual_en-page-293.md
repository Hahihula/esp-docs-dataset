
```markdown
Register 7.32. EFUSE_CLK_REG (0x01C8)


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

EFUSE_CLK_EN Configures whether to force enable eFuse register configuration clock signal.
1: Force
0: The clock is enabled only during the reading and writing of registers
(R/W)


Register 7.33. EFUSE_CONF_REG (0x01CC)


EFUSE_OP_CODE Configures operation command type.
0x5A5A: Program operation command
0x5AA5: Read operation command
Other values: No effect
(R/W)
```