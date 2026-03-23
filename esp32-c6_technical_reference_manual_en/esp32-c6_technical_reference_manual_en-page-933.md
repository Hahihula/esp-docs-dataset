
```markdown
Register 29.11. I2C_CTR_REG (0x0004)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 15  | I2C_ADDR_BROADCASTING_EN                                                   |
| 14  | I2C_ADDR_10BIT_RW_CHECK_EN                                                 |
| 13  | I2C_SIU_TX_AUTO_START_EN                                                    |
| 12  | I2C_CONF_UPGATE_TRANTION_EN                                                 |
| 11  | I2C_ESM_RST_CLK_EN                                                           |
| 10  | I2C_RX_LSB_FIRST                                                             |
| 9   | I2C_TX_LSB_FIRST                                                             |
| 8   | I2C_MS_MODE                                                                 |
| 7   | I2C_TRANS_START                                                              |
| 6   | I2C_RX_LSB_FIRST                                                             |
| 5   | I2C_RX_FULL_ACK_LEVEL                                                       |
| 4   | I2C_SAMPLE_SCL_LEVEL                                                        |
| 3   | I2C_SCL_FORCE_OUT                                                           |
| 2   | I2C_SDA_FORCE_OUT                                                            |
| 1   | Reset                                                                       |
| 0   | Reset                                                                       |

I2C_SDA_FORCE_OUT Configures the SDA output mode.
O: Open drain output
1: Direct output
(R/W)

I2C_SCL_FORCE_OUT Configures the SCL output mode.
O: Open drain output
1: Direct output
(R/W)

I2C_SAMPLE_SCL_LEVEL Configures the sample mode for SDA.
O: Sample SDA data on the SCL high level
1: Sample SDA data on the SCL low level
(R/W)

I2C_RX_FULL_ACK_LEVEL Configures the ACK value that needs to be sent by master when the rx_fifo_cnt has reached the threshold.
(R/W)

I2C_MS_MODE Configures the module as an I2C Master or Slave.
O: Slave
1: Master
(R/W)

I2C_TRANS_START Configures whether the slave starts sending the data in txfifo.
O: No effect
1: Start (WT)

I2C_TX_LSB_FIRST Configures to control the sending order for data needing to be sent.
O: send data from the most significant bit
1: send data from the least significant bit
(R/W)

I2C_RX_LSB_FIRST Configures to control the storage order for received data.
O: receive data from the most significant bit
1: receive data from the least significant bit
(R/W)
```