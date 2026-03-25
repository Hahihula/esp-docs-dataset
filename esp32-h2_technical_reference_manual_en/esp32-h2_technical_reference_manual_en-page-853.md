

```markdown
## 30.5.2.1 Introduction

Figure 30.5-2. I2Cmaster Writing to a Slave with a 10-bit Address

Figure 30.5-2 shows how I2Cmaster writes N bytes of data using 10-bit addressing to an I2C slave. The configuration and transfer process is similar to what is described in 30.5.1, except that a 10-bit I2Cslave address is formed from two bytes. Since a 10-bit I2Cslave address has one more byte than a 7-bit I2Cslave address, byte_num and length of data in TX RAM increase by 1 accordingly.

## 30.5.2.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
3. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|:------------------|:--------|:----------|:--------|:-------------|:---------|
| I2C_COMMAND0 (master) | RSTART | — | — | — | — |
| I2C_COMMAND1 (master) | WRITE | ack_value | ack_exp | 1 | N+2 |
| I2C_COMMAND2 (master) | STOP | — | — | — | — |

4. Configure I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) as I2Cslave’s 10-bit address, and set I2C_ADDR_10BIT_EN (slave) to 1 to enable 10-bit addressing.
5. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster. The first byte of the address of I2Cslave comprises ((0x78 | I2C_SLAVE_ADDR[9:8])<<1) and a R/W bit. The second byte of the address of I2Cslave is I2C_SLAVE_ADDR[7:0]. These two bytes are followed by data to be sent in FIFO or non-FIFO mode.
6. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
7. Write 1 to I2C_TRANS_START (master) and I2C_TRANS_START (slave) to start transfer.
```