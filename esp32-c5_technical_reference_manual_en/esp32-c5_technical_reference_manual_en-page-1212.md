

```markdown
Figure 34.7-1 shows how I2Cmaster writes N bytes of data to I2Cslave registers or RAM using 7-bit addressing. As shown in Figure 34.7-1, the first byte in the RAM of I2Cmaster is a 7-bit I2Cslave address followed by a R/W bit. When the R/W bit is 0, it indicates a WRITE operation. The remaining bytes are used to store data ready for transfer. The cmd box contains related command sequences.

After the command sequence is configured and data in RAM is ready, I2Cmaster enables the controller and initiates data transfer by setting the I2C_TRANS_START bit. The controller has four steps to take:

1. Wait for SCL to go high, to avoid SCL being used by other masters or slaves.
2. Execute a RSTART command by sending a START bit.
3. Execute a WRITE command by taking N+1 bytes from the RAM in order and sending them to I2Cslave in the same order. The first byte is the address of I2Cslave.
4. Execute a STOP command. Once the I2Cmaster transfers a STOP bit, an I2C_TRANS_COMPLETE_INT interrupt is generated.

34.71.2 Configuration Example

1. Configure the timing parameter registers of I2Cmaster and I2Cslave according to Section 34.4.7.
2. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command register | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master) | RSTART | — | — | — | — |
| I2C_COMMAND1 (master) | WRITE | ack_value | ack_exp | 1 | N+1 |
| I2C_COMMAND2 (master) | STOP | — | — | — | — |

5. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster in either FIFO mode or non-FIFO mode according to Section 34.4.10.
6. Write the address of I2Cslave to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.
7. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
8. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
9. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster's WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check the ACK value and take I2Cslave as a matching slave by default.

    * Match: If the received ACK value matches ack_exp (master) (the expected ACK value) in the WRITE command, I2Cmaster continues data transfer.
    * Not match: If the received ACK value does not match ack_exp in the WRITE command, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.

10. I2Cmaster sends data, and determines whether to check ACK value according to ack_check_en (master).
11. If data to be sent (N) is larger than TX FIFO depth, TX RAM of I2Cmaster may wrap around in FIFO mode. For details, please refer to Section 34.4.10.
```