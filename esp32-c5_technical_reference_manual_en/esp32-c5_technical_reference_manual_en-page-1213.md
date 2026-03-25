

```markdown
12. If data to be received (N) is larger than RX FIFO depth, RX RAM of I2C<sub>slave</sub> may wrap around in FIFO mode. For details, please refer to Section 34.4.10.

If data to be received (N) is larger than RX FIFO depth, the other way is to enable clock stretching by setting the I2C_SLAVE_SCL_STRETCH_EN (slave), and clearing I2C_RX_FULL_ACK_LEVEL. When RX RAM is full, an I2C_SLAVE_STRETCH_INT (slave) interrupt is generated. In this way, I2C<sub>slave</sub> can hold SCL low, in exchange for more time to read data. After the software has finished reading, you can set I2C_SLAVE_STRETCH_INT_CLR (slave) to 1 to clear interrupt, and set I2C_SLAVE_SCL_STRETCH_CLR (slave) to release the SCL line.

13. After data transfer completes, I2C<sub>master</sub> executes the STOP command, and generates an I2C_TRANS_COMPLETE_INIT (master) interrupt.
```

### 34.7.2 I2C<sub>master</sub> Writes to I2C<sub>slave</sub> with a 10-bit Address in One Command Sequence

#### 34.7.2.1 Introduction

Figure 34.7-2 shows how I2C<sub>master</sub> writes N bytes of data using 10-bit addressing to an I2C slave. The configuration and transfer process is similar to what is described in 34.7.1, except that a 10-bit I2C<sub>slave</sub> address is formed from two bytes. Since a 10-bit I2C<sub>slave</sub> address has one more byte than a 7-bit I2C<sub>slave</sub> address, byte_num and length of data in TX RAM increase by 1 accordingly.

#### 34.7.2.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
3. Configure command registers of I2C<sub>master</sub>.
```