

```markdown
Register 4.104. EFUSE_CONF_REG (0x01CC)

EFUSE_OP_CODE 0x5A5A: Operate programming command 0x5AA5: Operate read command.
(R/W)
```

```markdown
Register 4.105. EFUSE_CMD_REG (0x01D4)

EFUSE_READ_CMD Set this bit to send read command. (R/WS/SC)
EFUSE_PGM_CMD Set this bit to send programming command. (R/WS/SC)
EFUSE_BLK_NUM The serial number of the block to be programmed. Value 0-10 corresponds to
block number 0-10, respectively. (R/W)
```

```markdown
Register 4.106. EFUSE_DAC_CONF_REG (0x01E8)

EFUSE_DAC_CLK_DIV Controls the division factor of the rising clock of the programming voltage.
(R/W)
EFUSE_DAC_CLK_PAD_SEL Don't care. (R/W)
EFUSE_DAC_NUM Controls the rising period of the programming voltage. (R/W)
EFUSE_OE_CLR Reduces the power supply of the programming voltage. (R/W)
```