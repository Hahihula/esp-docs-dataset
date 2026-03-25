

```markdown
Register 30.24. I2C_INT_STATUS_REG (0x002C)

Continued from the previous page...

I2C_RXFIFO_UDF_INT_ST    The masked interrupt status of I2C_RXFIFO_UDF_INT. (RO)
I2C_SCL_ST_TO_INT_ST      The masked interrupt status of I2C_SCL_ST_TO_INT. (RO)
I2C_SCL_MAIN_ST_TO_INT_ST The masked interrupt status of I2C_SCL_MAIN_ST_TO_INT. (RO)
I2C_DET_START_INT_ST      The masked interrupt status of I2C_DET_START_INT. (RO)
I2C_SLAVE_STRETCH_INT_ST  The masked interrupt status of I2C_SLAVE_STRETCH_INT. (RO)
I2C_GENERAL_CALL_INT_ST   The masked interrupt status of I2C_GENERAL_CALL_INT. (RO)

I2C_SLAVE_ADDR_UNMATCH_INT_ST    The masked interrupt status of I2C_SLAVE_ADDR_UNMATCH_INT. (RO)


Register 30.25. I2C_COMDO_REG (0x0058)
```
```markdown
| 31 | 30 | ... | 14 | 13 | ... | 0 |
|-----|----|-----|----|----|-----|---|
| 0   | 0  | 0  | 0 | 0 | 0  | 0 | Reset
```
```markdown
I2C_COMMANDO Configures command 0.

It consists of three parts:
op_code is the command

1: WRITE
2: STOP
3: READ
4: END
6: RSTART

Byte_num represents the number of bytes that need to be sent or received.
ack_check_en, ack_exp, and ack are used to control the ACK bit. See I2C cmd structure 30.4-2 for more information.
(R/W)

I2C_COMMANDO_DONE Represents whether command 0 is done in I2C Master mode.

0: Not done
1: Done
(R/W/SS)
```