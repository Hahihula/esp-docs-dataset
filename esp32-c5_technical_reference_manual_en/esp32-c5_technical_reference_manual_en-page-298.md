

```markdown
Register 7.40. EFUSE_STATUS_REG (0x01D4)

EFUSE_STATE Represents the state of the eFuse state machine.
O: Reset state, the initial state after power-up
1: Idle state
Other values: Non-idle state
(RO)

EFUSE_BLK0_VALID_BIT_CNT Represents the number of block valid bit. (RO)
```

```markdown
Register 7.41. EFUSE_CMD_REG (0x01D8)

EFUSE_READ_CMD Configures whether to send read commands.
1: Send
O: No effect
(R/W/SC)

EFUSE_PGM_CMD Configures whether to send programming commands.
1: Send
O: No effect
(R/W/SC)

EFUSE_BLK_NUM Configures the serial number of the block to be programmed. Value 0-10 corresponds to block number 0-10, respectively. (R/W)
```