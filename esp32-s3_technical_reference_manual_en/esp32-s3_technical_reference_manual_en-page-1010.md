Title: Chapter 27 I2C Controller (I2C)

Subtitle: GoBack

Section Title: 27.5.7.2 Configuration Example

1. Set `I2C_MS_MODE` (master) to 1, and `I2C_MS_MODE` (slave) to 0.

2. We recommend setting `I2C_SLAVE_SCL_STRETCH_EN` (slave) to 1, so that SCL can be held low for more processing time when I2CSlave needs to send data. If this bit is not set, software should write data to be sent to I2CSlave’s TX RAM before I2Cmaster initiates transfer. Configuration below is applicable to scenario where `I2C_SLAVE_SCL_STRETCH_EN` (slave) is 1.

3. Set `I2C_FIFO_ADDR_CFGEN` to 1 to enable double addressing mode.

4. Write 1 to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) to synchronize registers.

5. Configure command registers of I2Cmaster.

Table:
- Command
- registers of I2Cmaster
- code
- ack_value
- ack_exp
- ack_check_en
- byte_num

| Command | registers of I2Cmaster | code | ack_value | ack_exp | ack_check_en | byte_num |
|---------|--------------------------|------|-----------|--------|--------------|---------|
| I2C COMMAND0 (master) | - | RESTART | — | 0 | N/A | – |
| I2C COMMAND1 (master) | WRITE | O | 0 | 1 | 1 | 2 |
| I2C COMMAND2 (master) | RESTART | — | — | — | — | — |
| I2C COMMAND3 (master) | WRITE | O | 0 | 1 | 1 | N-1 |
| I2C COMMAND4 (master) | READ | O | 0 | 1 | – | - |
| I2C COMMAND5 (master) | READ | — | 1 | 0 | 1 | 1 |
| I2C COMMAND6 (master) | STOP | N/A |——— | — | — | — |

6. Configure `I2C_SLAVE_ADDR` (slave) in `I2C_SLAVE_ADDR_REG` (slave) register as I2CSlave’s 7-bit address, and set `I2C_ADDR_10BIT_EN` to O to enable 7-bit addressing.

7. Write the address of I2CSlave and data to be sent to TX RAM of I2Cmaster in either FIFO or non-FIFO mode according to Section **27.4.10**. The first byte of address comprises (`I2C_SLAVE_ADDR[6:0]`<1>) and a `R/W` bit, which is O and indicates a WRITE. The second byte of address is memory address M of I2CSlave. The third byte is (`I2C_SLAVE_ADDR[6:0]`<1>) and an `R/W` bit, which is 1 and indicates a READ.

8. Write 1 to `I2C_CONF_UPGATE` (master) and `I2C_CONF_UPGATE` (slave) to synchronize registers.

9. Write 1 to `I2CTrans_START` (master) to start I2Cmaster’s transfer.

10. Start I2CSlave’s transfer according to Section **27.4.14**.

11. I2CSlave compares the slave address sent by I2Cmaster with its own address in `I2C_SLAVE_ADDR` (slave). When ack_check_en (master) in I2Cmaster’s WRITE command is 1, I2Cmaster checks ACK value each time it sends a byte. When ack_check_en (master) is O, I2Cmaster does not check ACK value and take I2CSlave as matching slave by default.

- Match: If the received ACK value matches `ack_exp` (master) (the expected ACK value), I2Cmaster continues data transfer.
  
Footer:
Espressif Systems
1010 ESP32-S3 TRM (Version 1.7)
Submit Documentation Feedback