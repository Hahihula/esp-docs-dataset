

```markdown
Register 34.46. LP_I2C_CTR_REG (0x0004)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30-1| LP_I2C_CONF_UPGATE                  | Configures this bit for synchronization. <br> O: No effect <br> 1: Synchronize (WT) |
| 29  | LP_I2C_ARBITRATION_EN               | Configures to enable I2C bus arbitration detection. <br> O: No effect <br> 1: Enable (R/W) |
| 28  | LP_I2C_FSM_RST                      | Configures to reset the SCL_FSM. <br> O: No effect <br> 1: Reset (WT)         |
| 27  | LP_I2C_CLK_EN                       | Configures whether to gate clock signal for registers. <br> O: Support clock only when registers are read or written to by software <br> 1: Force clock on for registers. (R/W) |
| 26  | LP_I2C_RX_FULL_ACK_LVL              | Configures the ACK value that needs to be sent by master when the rx_fifo_cnt has reached the threshold. (R/W) |
| 25  | LP_I2C_TRANS_START                  | Configures to start sending the data in TX FIFO for slave. <br> O: No effect <br> 1: Start (WT) |
| 24  | LP_I2C_TX_LSB_FIRST                 | Configures to control the sending order for data to be sent. <br> 1: send data from the least significant bit <br> O: send data from the most significant bit (R/W) |
| 23  | LP_I2C_RX_LSB_FIRST                 | Configures to control the storage order for received data. <br> 1: receive data from the least significant bit <br> O: receive data from the most significant bit (R/W) |
| 22-0| LP_I2C_SAMPLE_SCL_LEVEL             | Configures the sample mode for SDA. <br> 1: Sample SDA data on the SCL low level <br> O: Sample SDA data on the SCL high level. (R/W) |

LP_I2C_SAMPLE_SCL_LEVEL Configures the sample mode for SDA.
1: Sample SDA data on the SCL low level.
0: Sample SDA data on the SCL high level.
(R/W)

LP_I2C_RX_FULL_ACK_LVL Configures the ACK value that needs to be sent by master when the rx_fifo_cnt has reached the threshold. (R/W)

LP_I2C_TRANS_START Configures to start sending the data in TX FIFO for slave.
O: No effect
1: Start
(WT)

LP_I2C_TX_LSB_FIRST Configures to control the sending order for data to be sent.
1: send data from the least significant bit
O: send data from the most significant bit
(R/W)

LP_I2C_RX_LSB_FIRST Configures to control the storage order for received data.
1: receive data from the least significant bit
O: receive data from the most significant bit
(R/W)

LP_I2C_CLK_EN Configures whether to gate clock signal for registers.
O: Support clock only when registers are read or written to by software
1: Force clock on for registers.
(R/W)

LP_I2C_ARBITRATION_EN Configures to enable I2C bus arbitration detection.
O: No effect
1: Enable
(R/W)

LP_I2C_FSM_RST Configures to reset the SCL_FSM.
O: No effect
1: Reset
(WT)

LP_I2C_CONF_UPGATE Configures this bit for synchronization.
O: No effect
1: Synchronize (WT)
```