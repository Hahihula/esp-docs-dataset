

```markdown
Register 34.18. I2C_SR_REG (0x0008)

Continued from the previous page...

I2C_SCL_MAIN_STATE_LAST Represents the states of the I2C module state machine.

0: Idle
1: Address shift
2: ACK address
3: Rx data
4: Tx data
5: Send ACK
6: Wait ACK
7: Invalid
(RO)

I2C_SCL_STATE_LAST Represents the states of the state machine used to produce SCL.

0: Idle
1: Start
2: Negative edge
3: Low
4: rising edge
5: High
6: Stop
7: Invalid
(RO)

Register 34.19. I2C_FIFO_ST_REG (0x0014)
```
```markdown
| Bit | Name                  | Description                                                                 |
|-----|-----------------------|-----------------------------------------------------------------------------|
| 31  | reserved              |                                                                             |
| 30  |                       |                                                                             |
| 29  |                       |                                                                             |
| 22  | I2C_SLAVE_RW_POINT   | Represents the offset address in the I2C Slave RAM addressed by I2C Master when in I2C slave mode. (RO) |
| 21  | reserved              |                                                                             |
| 20  |                       |                                                                             |
| 19  |                       |                                                                             |
| 15  | I2C_TXFIFO_WADDR      | Represents the offset address of the APB bus writing to TX FIFO. (RO)        |
| 14  |                       |                                                                             |
| 10  | I2C_TXFIFO_RADDR      | Represents the offset address of the I2C module reading from TX FIFO. (RO)   |
| 9   | reserved              |                                                                             |
| 5   | I2C_RXFIFO_WADDR      | Represents the offset address of the APB reading from RX FIFO. (RO)          |
| 4   |                       |                                                                             |
| 0   | I2C_RXFIFO_RADDR      | Represents the offset address of the I2C module receiving data and writing to RX FIFO. (RO) |

Reset
```