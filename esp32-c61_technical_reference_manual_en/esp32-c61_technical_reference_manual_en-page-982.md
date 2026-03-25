

```markdown
| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:-------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMANDO (master) | ?START  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | —         | ack_exp | 1            | N+2       |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —            | —        |
```

```markdown
Chapter 27 I2C Controller (I2C)
GoBack

Figure 27.6-3 shows how I2Cmaster writes N bytes of data to I2Cslave registers or RAM using 7-bit double addressing. The configuration and transfer process is similar to what is described in Section 27.6.1, except that in 7-bit dual address mode I2Cmaster sends two 7-bit addresses. The first address is the address of an I2C slave, and the second one is I2Cslave’s memory address (i.e., addrM in Figure 27.6-3). When using double addressing, the slave RAM must be accessed in the non-FIFO mode, and clock stretching by the slave must be disabled. In the non-FIFO mode, the write pointer wraps around to the initial position of the FIFO once its depth is exceeded. As a consequence, data in the slave’s RAM is overwritten cyclically every 32 bytes. When new data is written to an address that already contains data in the slave, the existing data is directly overwritten without any warning or error indication.

27.6.3.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Set I2C_FIFO_ADDR_CFG_EN (slave) to 1 to enable dual address mode.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|:-------------------|:---------|:-----------|:---------|:--------------|:----------|
| I2C_COMMANDO (master) | ?START  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | —         | ack_exp | 1            | N+2       |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —            | —        |

5. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster in FIFO or non-FIFO mode.
6. Write the address of I2Cslave to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.
7. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
8. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
9. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is 0, I2Cmaster does not check ACK value and takes I2Cslave as a matching slave by default.

* Match: If the received ACK value matches ack_exp (master) (the expected ACK value), I2Cmaster continues data transfer.
* Not match: If the received ACK value does not match ack_exp, I2Cmaster generates an I2C_NACK_INT (master) interrupt and stops data transfer.

10. I2Cslave receives the RX RAM address sent by I2Cmaster and adds the offset.
11. I2Cmaster sends data, and determines whether to check ACK value according to ack_check_en (master).
12. If data to be sent is larger than TX FIFO depth, TX RAM of I2Cmaster may wrap around in FIFO mode. For details, please refer to Section 27.4.10.
13. After data transfer completes, I2Cmaster executes the STOP command, and generates an I2C_TRANS_COMPLETE_INT (master) interrupt.

Espressif Systems
982
ESP32-C61 TRM (Pre-release v0.5)
Submit Documentation Feedback PRELIMINARY
```