

```markdown
Register 29.18. I2C_SR_REG (0x0008)

Continued from the previous page...

I2C_SCL_MAIN_STATE_LAST Represents the states of the I2C module state machine.
- 0: Idle
- 1: Address shift
- 2: ACK address
- 3: Rx data
- 4: Tx data
- 5: Send ACK
- 6: Wait ACK (RO)

I2C_SCL_STATE_LAST Represents the states of the state machine used to produce SCL.
- 0: Idle
- 1: Start
- 2: Negative edge
- 3: Low
- 4: Positive edge
- 5: High
- 6: Stop (RO)

Register 29.19. I2C_FIFO_ST_REG (0x0014)

| 31 | 30 | 29             | 22 | 21 | 20 | 19       | 18        | 15 | 14      | 10 | 9         | 5   | 4          | 0           |
|----|----|----------------|----|----|----|----------|-----------|----|---------|----|-----------|-----|------------|-------------|
|    |    | (reserved)    |    |    |    | (reserved)| I2C_SLAVE_RW_POINT | I2C_TXFIFO_WADDR | 15 | 14      | 10 | 9         | 5   | 4          | 0           |
|    |    |                |    |    |    |          |            |    |         |    |           |     |            |             |
| 0  | 0  | I2C_SLAVE_RW_POINT | 0  | 0  |    | O        | O         | O  | O      | O   | O         | O   | O          | Reset       |

I2C_RXFIFO_RADDR Represents the offset address of the APB reading from RXFIFO. (RO)

I2C_RXFIFO_WADDR Represents the offset address of i2c module receiving data and writing to RXFIFO. (RO)

I2C_TXFIFO_RADDR Represents the offset address of i2c module reading from TXFIFO. (RO)

I2C_TXFIFO_WADDR Represents the offset address of APB bus writing to TXFIFO. (RO)

I2C_SLAVE_RW_POINT Represents the offset address in the I2C Slave RAM addressed by I2C Master when in I2C slave mode. (RO)
```