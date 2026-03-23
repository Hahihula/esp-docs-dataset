

```markdown
Register 6.105. EFUSE_STATUS_REG (0x01D0)

EFUSE_STATE Represents the state of the eFuse state machine. (RO)
EFUSE_BLK0_VALID_BIT_CNT Represents the number of block valid bit. (RO)

Register 6.106. EFUSE_CMD_REG (0x01D4)

EFUSE_READ_CMD Configures whether or not to send read command.
    1: Send
    0: No effect
    (R/W/SC)

EFUSE_PGM_CMD Configures whether or not to send programming command.
    1: Send
    0: No effect
    (R/W/SC)

EFUSE_BLK_NUM Represents the serial number of the block to be programmed. Value 0-10 corresponds to block number 0-10, respectively. (R/W)
```