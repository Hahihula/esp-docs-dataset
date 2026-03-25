

```markdown
Register 30.11. I2C_CTR_REG (0x0004)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 15  | I2C_ADDR_BROADCASTING_EN                                                   |
| 14  | I2C_ADDR_10BIT_RW_CHECK_EN                                                 |
| 13  | I2C_AUTO_START_EN                                                           |
| 12  | I2C_CONF_UPGATE_TRNTRATION_EN                                               |
| 11  | I2C_SIU_TX_LSB_FIRST                                                        |
| 10  | I2C_FSM_RST_CLK_EN                                                          |
| 9   | I2C_RX_LSB_FIRST                                                             |
| 8   | I2C_TX_LSB_FIRST                                                             |
| 7   | I2C_MS_MODE                                                                 |
| 6   | I2C_RX_FULL_ACK_LEVEL                                                       |
| 5   | I2C_SAMPLE_SCL_LEVEL                                                        |
| 4   | I2C_SDA_FORCE_OUT                                                           |
| 3   | I2C_SCL_FORCE_OUT                                                           |
| 2   | (reserved)                                                                  |
| 1   | (reserved)                                                                  |
| 0   | Reset                                                                      |

I2C_SDA_FORCE_OUT Configures the SDA output mode.
- 0: Open drain output
- 1: Direct output
(R/W)

I2C_SCL_FORCE_OUT Configures the SCL output mode.
- 0: Open drain output
- 1: Direct output
(R/W)

I2C_SAMPLE_SCL_LEVEL Configures the sample mode for SDA.
- 0: Sample SDA data on the SCL high level
- 1: Sample SDA data on the SCL low level
(R/W)

I2C_RX_FULL_ACK_LEVEL Configures the ACK value that needs to be sent by master when rx_fifo_cnt has reached the threshold.
(R/W)

I2C_MS_MODE Configures the module as an I2C Master or Slave.
- 0: Slave
- 1: Master
(R/W)

I2C_TRANS_START Configures whether the slave starts sending the data in TX FIFO.
- 0: No effect
- 1: Start (WT)

I2C_TX_LSB_FIRST Configures whether or not to control the sending order for data needing to be sent.
- 0: Send data from the most significant bit
- 1: Send data from the least significant bit
(R/W)

I2C_RX_LSB_FIRST Configures whether or not to control the storage order for received data.
- 0: Receive data from the most significant bit
- 1: Receive data from the least significant bit
(R/W)

Continued on the next page...
```