

```markdown
## 44.6.1.1 Introduction

Figure 44.6-1. I2Cmaster Writing to I2Cslave with a 7-bit Address

Master

cmd | op_code | byte_num
----|---------|---------
cmd0| RSTART  |
cmd1| WRITE   | N+1
cmd2| STOP    |

RAM addr0 (slave_addr<<1 | r/w)
addr1 | byte0
addr2 | byte1
...   | byte(N-1)

Slave

RAM addr0 | byte0
addr1     | byte1
addr2     | ...
addrN-1   | byte(N-1)

SDA SCL

Figure 44.6-1 shows how I2Cmaster writes N bytes of data to I2Cslave registers or RAM using 7-bit addressing. As shown in figure 44.6-1, the first byte in the RAM of I2Cmaster is a 7-bit I2Cslave address followed by a R/W bit. When the R/W bit is 0, it indicates a WRITE operation. The remaining bytes are used to store data ready for transfer. The cmd box contains related command sequences.

After the command sequence is configured and data in RAM is ready, I2Cmaster enables the controller and initiates data transfer by setting the I2C_TRANS_START bit. The controller has four steps to take:

1. Wait for SCL to go high, to avoid SCL being used by other masters or slaves.
2. Execute a RSTART command by sending a START bit.
3. Execute a WRITE command by taking N+1 bytes from the RAM in order and sending them to I2Cslave in the same order. The first byte is the address of I2Cslave.
4. Execute a STOP command. Once the I2Cmaster transfers a STOP bit, an I2C_TRANS_COMPLETE_INT interrupt is generated.

## 44.6.1.2 Configuration Example

1. Configure the timing parameter registers of I2Cmaster and I2Cslave according to Section 44.4.7.
2. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command register | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master) | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | —         | ack_exp | 1            | N+1      |
```