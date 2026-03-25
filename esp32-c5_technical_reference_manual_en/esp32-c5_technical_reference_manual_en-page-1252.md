

```markdown
Register 34.25. I2C_COMDO_REG (0x0058)

| Bit | Description       |
|-----|-------------------|
| 31  | (reserved)        |
| 30  |                   |
| ... |                   |
| 14  |                   |
| 13  |                   |
| 0   | Reset             |

I2C_COMMANDO Configures command 0.
It consists of three parts:
op_code is the command
1: WRITE
2: STOP
3: READ
4: END
6: RSTART

Byte_num represents the number of bytes that need to be sent or received.
ack_check_en, ack_exp, and ack are used to control the ACK bit. See I2C cmd structure 34.4-2 for more information.
(R/W)

I2C_COMMANDO_DONE Represents whether command 0 is done in I2C Master mode.
0: Not done
1: Done
(R/W/SS)
```

```markdown
Register 34.26. I2C_COMD1_REG (0x005C)

| Bit | Description       |
|-----|-------------------|
| 31  | (reserved)        |
| 30  |                   |
| ... |                   |
| 14  |                   |
| 13  |                   |
| 0   | Reset             |

I2C_COMMAND1 Configures command 1.
See details in I2C_COMMANDO. (R/W)

I2C_COMMAND1_DONE Represents whether command 1 is done in I2C Master mode.
0: Not done
1: Done
(R/W/SS)
```