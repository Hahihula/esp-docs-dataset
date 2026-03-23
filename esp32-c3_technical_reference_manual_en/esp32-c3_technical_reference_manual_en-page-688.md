

```markdown
## 28.5.1.1 Introduction

Figure 28.5-1 shows how I2C_master writes N bytes of data to I2C_slave’s RAM using 7-bit addressing. As shown in figure 28.5-1, the first byte in the RAM of I2C_master is a 7-bit I2C_slave address followed by a R/W bit. When the R/W bit is 0, it indicates a WRITE operation. The remaining bytes are used to store data ready for transfer. The cmd box contains related command sequences.

After the command sequence is configured and data in RAM is ready, I2C_master enables the controller and initiates data transfer by setting the I2C_TRANS_START bit. The controller has four steps to take:

1. Wait for SCL to go high, to avoid SCL being used by other masters or slaves.
2. Execute a RSTART command and send a START bit.
3. Execute a WRITE command by taking N+1 bytes from the RAM in order and send them to I2C_slave in the same order. The first byte is the address of I2C_slave.
4. Send a STOP. Once the I2C_master transfers a STOP bit, an I2C_TRANS_COMPLETE_INT interrupt is generated.

## 28.5.1.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
3. Configure command registers of I2C_master.

| Command register | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMAND0 (master) | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | ack_value | ack_exp | 1            | N+1      |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —            | —        |
```