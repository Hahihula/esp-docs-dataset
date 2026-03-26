

```markdown
Register 44.51. LP_I2C_SR_REG (0x0008)

| Bit | 31 | 30 | 28 | 27 | 26 | 24 | 23 | 22 | 18 | 17 | 13 | 12 | 8 | 7 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|----|----|----|----|----|----|----|----|----|----|----|----|---|---|---|---|---|---|---|---|
|     | O  | O  | O  | O  | O  | O  | O  | O  | O  | O  | O  | O  | O | O | O | O | O | O | O | Reset |

LP_I2C_RESP_REC Represents the received ACK value in master mode or slave mode.
0: ACK
1: NACK (RO)

LP_I2C_ARB_LOST Represents whether the I2C controller loses control of SCL line.
0: No arbitration lost
1: Arbitration lost (RO)

LP_I2C_BUS_BUSY Represents the I2C bus state.
1: The I2C bus is busy transferring data
0: The I2C bus is in idle state (RO)

LP_I2C_RXFIFO_CNT Represents the number of data bytes received in RAM. (RO)

LP_I2C_TXFIFO_CNT Represents the number of data bytes to be sent. (RO)

LP_I2C_SCL_MAIN_STATE_LAST Represents the states of the I2C module state machine.
0: Idle
1: Address shift
2: ACK address
3: Rx data
4: Tx data
5: Send ACK
6: Wait ACK (RO)

LP_I2C_SCL_STATE_LAST Represents the states of the state machine used to produce SCL.
0: Idle
1: Start
2: Negative edge
3: Low
4: Positive edge
5: High
6: Stop (RO)
```