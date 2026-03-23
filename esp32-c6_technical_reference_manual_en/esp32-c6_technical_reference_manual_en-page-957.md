

```markdown
Register 29.46. LP_I2C_CTR_REG (0x0004)

| Bit | Name                                 | Description                                                                 |
|-----|--------------------------------------|-----------------------------------------------------------------------------|
| 31  | (reserved)                          |                                                                             |
| 30-1| LP_I2C_SAMPLE_SCL_LEVEL             | Configures the sample mode for SDA.<br>1: Sample SDA data on the SCL low level.<br>0: Sample SDA data on the SCL high level.<br>(R/W) |
| 29  | LP_I2C_RX_FULL_ACK_LEVEL            | Configures the ACK value that needs to be sent by master when the rx_fifo_cnt has reached the threshold. (R/W) |
| 28  | LP_I2C_TRANS_START                  | Configures to start sending the data in txfifo for slave.<br>0: No effect<br>1: Start<br>(WT) |
| 27  | LP_I2C_TX_LSB_FIRST                 | Configures to control the sending order for data to be sent.<br>1: send data from the least significant bit<br>0: send data from the most significant bit<br>(R/W) |
| 26  | LP_I2C_RX_LSB_FIRST                 | Configures to control the storage order for received data.<br>1: receive data from the least significant bit<br>0: receive data from the most significant bit<br>(R/W) |
| 25  | LP_I2C_CLK_EN                       | Configures whether to gate clock signal for registers.<br>0: Support clock only when registers are read or written to by software<br>1: Force clock on for registers.<br>(R/W) |
| 24  | LP_I2C_ARBITRATION_EN               | Configures to enable I2C bus arbitration detection.<br>0: No effect<br>1: Enable<br>(R/W) |
| 23  | LP_I2C_FSM_RST                      | Configures to reset the SCL FSM.<br>0: No effect<br>1: Reset<br>(WT) |
| 22  | LP_I2C_CONF_UPGATE                  | Configures this bit for synchronization.<br>0: No effect<br>1: Synchronize<br>(WT) |
```