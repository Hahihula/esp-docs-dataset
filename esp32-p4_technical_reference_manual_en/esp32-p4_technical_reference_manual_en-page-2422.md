

```markdown
Register 44.46. LP_I2C_CTR_REG (0x0004)

LP_I2C_SAMPLE_SCL_LEVEL Configures the sample mode for SDA.
1: Sample SDA data on the SCL low level.
0: Sample SDA data on the SCL high level.
(R/W)

LP_I2C_RX_FULL_ACK_LEVEL Configures the ACK value that needs to be sent by master when the rx_fifo_cnt has reached the threshold. (R/W)

LP_I2C_TRANS_START Configures to start sending the data in txfifo for slave.
0: No effect
1: Start
(WT)

LP_I2C_TX_LSB_FIRST Configures to control the sending order for data to be sent.
1: send data from the least significant bit
0: send data from the most significant bit
(R/W)

LP_I2C_RX_LSB_FIRST Configures to control the storage order for received data.
1: receive data from the least significant bit
0: receive data from the most significant bit
(R/W)

LP_I2C_CLK_EN Configures whether to gate clock signal for registers.
0: Support clock only when registers are read or written to by software
1: Force clock on for registers.
(R/W)

LP_I2C_ARBITRATION_EN Configures to enable I2C bus arbitration detection.
0: No effect
1: Enable
(R/W)

LP_I2C_FSM_RST Configures to reset the SCL_FSM.
0: No effect
1: Reset
(WT)

LP_I2C_CONF_UPGATE Configures this bit for synchronization.
0: No effect
1: Synchronize
```