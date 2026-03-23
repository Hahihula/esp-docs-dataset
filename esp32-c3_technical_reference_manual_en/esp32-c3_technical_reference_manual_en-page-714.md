

```markdown
Register 28.11. I2C_CTR_REG (0x0004)

| Bit | Description                                                                 |
|-----|-----------------------------------------------------------------------------|
| 31  | (reserved)                                                                  |
| 15  | I2C_ADDR_BROADCASTING_EN                                                   |
| 14  | I2C_ADDR_10BIT_RW_CHECK_EN                                                 |
| 13  | I2C_SLV_TX_AUTO_START_EN                                                    |
| 12  | I2C_CONF_UPGATE                                                              |
| 11  | I2C_FSM_RST                                                                  |
| 10  | I2C_CLK_EN                                                                   |
| 9   | I2C_RX_LSB_FIRST                                                             |
| 8   | I2C_TX_LSB_FIRST                                                             |
| 7   | I2C_MS_MODE                                                                  |
| 6   | I2C_TRANS_START                                                              |
| 5   | I2C_RX_FULL_ACK_LEVEL                                                       |
| 4   | I2C_SAMPLE_SCL_LEVEL                                                        |
| 3   | I2C_SCL_FORCE_OUT                                                            |
| 2   | I2C_SDA_FORCE_OUT                                                            |
| 1   | Reset                                                                       |

I2C_SDA_FORCE_OUT Configures the SDA output mode.
0: Open drain output
1: Direct output
(R/W)

I2C_SCL_FORCE_OUT Configures the SCL output mode.
0: Open drain output
1: Direct output
(R/W)

I2C_SAMPLE_SCL_LEVEL This bit is used to select the sampling mode. 0: samples SDA data on the SCL high level; 1: samples SDA data on the SCL low level. (R/W)

I2C_RX_FULL_ACK_LEVEL This bit is used to configure the ACK value that need to be sent by master when I2C_RXFIFO_CNT has reached the threshold. (R/W)

I2C_MS_MODE Set this bit to configure the I2C controller as an I2C Master. Clear this bit to configure the I2C controller as a slave. (R/W)

I2C_TRANS_START Set this bit to start sending the data in TX FIFO. (WT)

I2C_TX_LSB_FIRST This bit is used to control the order to send data. 0: sends data from the most significant bit; 1: sends data from the least significant bit. (R/W)

I2C_RX_LSB_FIRST This bit is used to control the order to receive data. 0: receives data from the most significant bit; 1: receives data from the least significant bit. (R/W)

I2C_CLK_EN This field controls APB_CLK clock gating. 0: APB_CLK is gated to save power; 1: APB_CLK is always on. (R/W)

I2C_ARBITRATION_EN This is the enable bit for I2C bus arbitration function. (R/W)

I2C_FSM_RST This bit is used to reset the SCL FSM. (WT)

I2C_CONF_UPGATE Synchronization bit. (WT)

I2C_SLV_TX_AUTO_START_EN This is the enable bit for slave to send data automatically. (R/W)

I2C_ADDR_10BIT_RW_CHECK_EN This is the enable bit to check if the R/W bit of 10-bit addressing is consistent with the I2C protocol. (R/W)

I2C_ADDR_BROADCASTING_EN This is the enable bit for 7-bit general call addressing. (R/W)
```