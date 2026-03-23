

```markdown
## 29.6.2 I2Cmaster Writes to I2Cslave with a 10-bit Address in One Command Sequence

### 29.6.2.1 Introduction

Figure 29.6-2 shows how I2Cmaster writes N bytes of data using 10-bit addressing to an I2C slave. The configuration and transfer process is similar to what is described in 29.6.1, except that a 10-bit I2Cslave address is formed from two bytes. Since a 10-bit I2Cslave address has one more byte than a 7-bit I2Cslave address, byte_num and length of data in TX RAM increase by 1 accordingly.

### 29.6.2.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Write 1 to I2C_CONF_UPDATE (master) and I2C_CONF_UPDATE (slave) to synchronize registers.
3. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|-------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO      | RSTART  | —         | —       | —            | —        |
| I2C_COMMAND1 (master) | WRITE   | ack_value | ack_exp | 1            | N+2      |
| I2C_COMMAND2 (master) | STOP    | —         | —       | —            | —        |

4. Configure I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) as I2Cslave’s 10-bit address, and set I2C_ADDR_10BIT_EN (slave) to 1 to enable 10-bit addressing.
5. Write the address of I2Cslave and data to be sent to TX RAM of I2Cmaster. The first byte of the address of I2Cslave comprises ((0x78 | I2C_SLAVE_ADDR[9:8])<<1) and a R/W bit. The second byte of the address of
```