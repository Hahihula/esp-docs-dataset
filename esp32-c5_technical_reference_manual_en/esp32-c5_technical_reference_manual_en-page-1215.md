

```markdown
## Chapter 34 I2C Controller (I2C)

### 34.7.3.1 Introduction

Figure 34.7-3. I2Cmaster Writing to I2Cslave with Two 7-bit Addresses

Figure 34.7-3 shows how I2Cmaster writes N bytes of data to I2Cslave registers or RAM using 7-bit double addressing. The configuration and transfer process is similar to what is described in Section 34.7.1, except that in 7-bit dual address mode I2Cmaster sends two 7-bit addresses. The first address is the address of an I2C slave, and the second one is I2Cslave’s memory address (i.e., addrM in Figure 34.7-3). When using double addressing, RAM must be accessed in non-FIFO mode. The I2C slave puts received byte0 ~ byte (N-1) into its RAM in an order starting from addrM. The RAM is overwritten every 32 bytes.

### 34.7.3.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Set I2C_FIFO_ADDR_CFG_EN (slave) to 1 to enable dual address mode.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_en | byte_num |
|-------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master) | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | ack_value | ack_exp | 1            | N+2      |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —            | —        |

5. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster in FIFO or non-FIFO mode.
6. Write the address of I2Cslave to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.
7. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
8. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
9. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it
```