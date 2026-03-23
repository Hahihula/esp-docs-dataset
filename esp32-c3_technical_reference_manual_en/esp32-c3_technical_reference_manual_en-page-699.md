

```markdown
Figure 28.5-6 shows how I2Cmaster reads data from an I2C slave using 10-bit addressing. Unlike 7-bit addressing, in 10-bit addressing the WRITE command of the I2Cmaster is formed from two bytes, and correspondingly TX RAM of this master stores a 10-bit address of two bytes. The R/W bit in the first byte is 0, which indicates a WRITE operation. After a RSTART condition, I2Cmaster sends the first byte of address again to read data from I2Cslave, but the R/W bit is 1, which indicates a READ operation. The two address bytes can be configured as described in Section 28.5.2.

28.5.6.2 Configuration Example

1. Set I2C_MS_MODE (master) to 1, and I2C_MS_MODE (slave) to 0.
2. We recommend setting I2C_SLAVE_SCL_STRETCH_EN (slave) to 1, so that SCL can be held low for more processing time when I2Cslave needs to send data. If this bit is not set, software should write data to be sent to I2Cslave’s TX RAM before I2Cmaster initiates transfer. Configuration below is applicable to scenario where I2C_SLAVE_SCL_STRETCH_EN (slave) is 1.
3. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
4. Configure command registers of I2Cmaster.

| Command registers | op_code | ack_value | ack_exp | ack_check_er | byte_num |
|-------------------|---------|-----------|---------|--------------|----------|
| I2C_COMMANDO (master) | RSTART | — | — | — | — |
| I2C_COMMAND1(master) | WRITE | 0 | 0 | 1 | 2 |
| I2C_COMMAND2(master) | RSTART | — | — | — | — |
| I2C_COMMAND3(master) | WRITE | 0 | 0 | 1 | 1 |
| I2C_COMMAND4(master) | READ | 0 | 0 | 1 | N-1 |
| I2C_COMMAND5(master) | READ | 1 | 0 | 1 | 1 |
| I2C_COMMAND6(master) | STOP | — | — | — | — |

5. Configure I2C_SLAVE_ADDR (slave) in I2C_SLAVE_ADDR_REG (slave) as I2Cslave’s 10-bit address, and set I2C_ADDR_10BIT_EN (slave) to 1 to enable 10-bit addressing.
6. Write I2Cslave address and data to be sent to TX RAM of I2Cmaster in either FIFO or non-FIFO mode. The first byte of address comprises ((0x78 | I2C_SLAVE_ADDR[9:8])<<1) and a R/W bit, which is 1 and indicates a WRITE operation. The second byte of address is I2C_SLAVE_ADDR[7:0]. The third byte is ((0x78 | I2C_SLAVE_ADDR[9:8])<<1) and a R/W bit, which is 1 and indicates a READ operation.
7. Write 1 to I2C_CONF_UPGATE (master) and I2C_CONF_UPGATE (slave) to synchronize registers.
8. Write 1 to I2C_TRANS_START (master) to start I2Cmaster’s transfer.
9. Start I2Cslave’s transfer according to Section 28.4.14.
10. I2Cslave compares the slave address sent by I2Cmaster with its own address in I2C_SLAVE_ADDR (slave). When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it
```