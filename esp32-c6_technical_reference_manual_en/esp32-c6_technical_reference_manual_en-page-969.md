

```markdown
Register 29.58. LP_I2C_COMDO_REG (0x0058)

LP_I2C_COMMANDO Configures command O.

It consists of three parts:
op_code is the command
0: RSTART
1: WRITE
2: READ
3: STOP
4: END.
Byte_num represents the number of bytes that need to be sent or received.
ack_check_en, ack_exp and ack are used to control the ACK bit. See I2C cmd structure 29.4-2 for more information. (R/W)

LP_I2C_COMMANDO_DONE Represents whether command O is done in I2C Master mode.
0: Not done
1: Done
(R/W/SS)
```

```markdown
Register 29.59. LP_I2C_COMD1_REG (0x005C)

LP_I2C_COMMAND1 Configures command 1.
See details in I2C_CMD0_REG[13:O]. (R/W)

LP_I2C_COMMAND1_DONE Represents whether command 1 is done in I2C Master mode.
0: Not done
1: Done
(R/W/SS)
```