

```markdown
Register 5.39. EFUSE_STATUS_REG (0x01D0)

EFUSE_STATE Represents the state of the eFuse state machine. (RO)
EFUSE_OTP_LOAD_SW Represents the value of OTP_LOAD_SW. (RO)
EFUSE_OTP_VDDQ_C_SYNC2 Represents the value of OTP_VDDQ_C_SYNC2. (RO)
EFUSE_OTP_STROBE_SW Represents the value of OTP_STROBE_SW. (RO)
EFUSE_OTP_CSB_SW Represents the value of OTP_CSB_SW. (RO)
EFUSE_OTP_PGENB_SW Represents the value of OTP_PGENB_SW. (RO)
EFUSE_OTP_VDDQ_IS_SW Represents the value of OTP_VDDQ_IS_SW. (RO)
EFUSE_BLK0_VALID_BIT_CNT Represents the number of valid block bits. (RO)
EFUSE_CUR_ECDSA_BLK Represents the block used for ECDSA key output. (RO)

Register 5.40. EFUSE_CMD_REG (0x01D4)

EFUSE_READ_CMD Configures whether to send read command.
1: Send
O: No effect
(R/W/SC)

EFUSE_PGM_CMD Configures whether to send programming command.
1: Send
O: No effect
(R/W/SC)

EFUSE_BLK_NUM Represents the serial number of the block to be programmed. Value 0-10 corresponds to block number 0-10, respectively. (R/W)
```