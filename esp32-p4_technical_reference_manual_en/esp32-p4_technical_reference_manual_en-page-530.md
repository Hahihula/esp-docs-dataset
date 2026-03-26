

```markdown
## Register 8.39. EFUSE_CMD_REG (0x01D4)

EFUSE_READ_CMD Configures whether to send read commands.
- 1: Send
- 0: No effect
(R/W/SC)

EFUSE_PGM_CMD Configures whether to send programming commands.
- 1: Send
- 0: No effect
(R/W/SC)

EFUSE_BLK_NUM Represents the serial number of the block to be programmed. Value 0-10 corresponds to block number 0-10, respectively. (R/W)
```

```markdown
## Register 8.40. EFUSE_INT_RAW_REG (0x01D8)

EFUSE_READ_DONE_INT_RAW The raw interrupt status of EFUSE_READ_DONE_INT. (R/SS/WTC)

EFUSE_PGM_DONE_INT_RAW The raw interrupt status of EFUSE_PGM_DONE_INT. (R/SS/WTC)
```