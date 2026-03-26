

```markdown
## 44.6.2.1 Introduction

Figure 44.6-2. I2Cmaster Writing to a Slave with a 10-bit Address

Master

cmd | op_code | byte_num
----|---------|---------
cmd0| RSTART  |
cmd1| WRITE   | N+2
cmd2| STOP    |

RAM addr0 (slave_addr_first_7bits<<1|r/w)
addr1 slave_addr_second_byte
addr2 byte0
...
addr(N+1) byte(N-1)

Slave

RAM addr0 byte0
addr1 byte1
addr2 ...
addr(N-1) byte(N-1)

SCL SDA

Figure 44.6-2 shows how I2Cmaster writes N bytes of data using 10-bit addressing to an I2C slave. The configuration and transfer process is similar to what is described in 44.6.1, except that a 10-bit I2Cslave address is formed from two bytes. Since a 10-bit I2Cslave address has one more byte than a 7-bit I2Cslave address, byte_num and length of data in TX RAM increase by 1 accordingly.

## 44.6.2.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
3. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|-------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMAND0 (master) | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | —         | ack_exp | 1            | N+2       |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —            | —        |

4. Configure I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) as I2Cslave’s 10-bit address, and set I2C_ADDR_10BIT_EN (slave) to 1 to enable 10-bit addressing.
5. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster. The first byte of the address of I2Cslave comprises ((0x78 | I2C_SLAVE_ADDR[9:8])<<1) and a R/W bit. The second byte of the address of I2Cslave is I2C_SLAVE_ADDR[7:0]. These two bytes are followed by data to be sent in FIFO or non-FIFO mode.
6. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
7. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
```