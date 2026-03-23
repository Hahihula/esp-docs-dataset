

```markdown
## 28.5.3 I2Cmaster Writes to I2Cslave with Two 7-bit Addresses in One Command Sequence

### 28.5.3.1 Introduction

Figure 28.5-3 shows how I2Cmaster writes N bytes of data to I2Cslave’s RAM using 7-bit double addressing. The configuration and transfer process is similar to what is described in Section 28.5.1, except that in 7-bit double addressing mode I2Cmaster sends two 7-bit addresses. The first address is the address of an I2C slave, and the second one is I2Cslave’s memory address (i.e. addrM in Figure 28.5-3). When using double addressing, RAM must be accessed in non-FIFO mode. The I2C slave put received byte0 ~ byte(N-1) into its RAM in an order staring from addrM. The RAM is overwritten every 32 bytes.

### 28.5.3.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Set I2C_FIFO_ADDR_CFG_EN (slave) to 1 to enable double addressing mode.
3. Write 1 to I2C_CONF_UPGRADE (master) and I2C_CONF_UPGRADE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|:------------------|:--------|:----------|:--------|:-------------|:---------|
| I2C_COMMANDO (master) | RSTART | —        | —      | —           | —       |
| I2C_COMMAND1 (master) | WRITE  | ack_value | ack_exp | 1           | N+2     |
| I2C_COMMAND2 (master) | STOP   | —        | —      | —           | —       |

5. Write I2Cslave address and data to be sent to TX RAM of I2Cmaster in FIFO or non-FIFO mode.
6. Write address of I2Cslave to I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) register.
```